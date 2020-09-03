---
title: PowerShell 작업에서 Azure PowerShell cmdlet 실행
description: -AsJob 및 Start-Job을 사용하여 Azure PowerShell cmdlet을 병렬 또는 백그라운드 작업으로 실행하는 방법에 대해 알아보세요.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 5d9028c0a433149c8f6cc346651bb8bf875bb42a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89240916"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a>PowerShell 작업에서 Azure PowerShell cmdlet 실행

Azure PowerShell은 Azure Cloud에 연결하고 응답을 기다리는 방법에 따라 달라지므로 대부분의 cmdlet은 클라우드에서 응답을 받을 때까지 PowerShell 세션을 차단합니다.
Powershell 작업을 사용하면 백그라운드에서 cmdlet을 실행하거나 단일 PowerShell 세션 내에서 Azure의 여러 작업을 한 번에 수행할 수 있습니다.

이 문서는 Azure PowerShell cmdlet을 PowerShell 작업으로 실행하고 완료 여부를 확인하는 방법에 대한 간략한 개요입니다. Azure PowerShell에서 명령을 실행하려면 [Azure 컨텍스트 및 로그인 자격 증명](context-persistence.md)에서 자세히 설명된 Azure PowerShell 컨텍스트를 사용해야 합니다.
PowerShell 작업에 대한 자세한 내용은 [PowerShell 작업 정보](/powershell/module/microsoft.powershell.core/about/about_jobs)를 참조하세요.

## <a name="azure-contexts-with-powershell-jobs"></a>PowerShell 작업을 사용하는 Azure 컨텍스트

PowerShell 작업은 연결된 PowerShell 세션 없이 별도의 프로세스로서 실행되므로 Azure 자격 증명을 공유해야 합니다. 자격 증명은 다음 메서드 중 하나를 사용하여 Azure 컨텍스트 개체로 전달됩니다.

* 자동 컨텍스트 지속성. 컨텍스트 지속성은 기본적으로 사용되며 여러 세션에서 로그인 정보를 유지합니다. 컨텍스트 지속성을 사용하면 현재 Azure 컨텍스트가 새 프로세스에 전달됩니다.

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* Azure PowerShell cmdlet과 함께 `-AzContext` 매개 변수를 사용하여 Azure 컨텍스트 개체를 제공합니다.

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  컨텍스트 지속성을 사용하지 않는 경우 `-AzContext` 인수가 필요합니다.

* 일부 Azure PowerShell cmdlet에서 제공하는 `-AsJob` 스위치를 사용합니다. 이 스위치는 현재 활성 Azure 컨텍스트를 사용하여 cmdlet을 PowerShell 작업으로 자동 시작합니다.

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  cmdlet이 `-AsJob`을 지원하는지 확인하려면 해당 참조 설명서를 확인하세요. `-AsJob` 스위치는 컨텍스트 자동 저장을 사용하도록 설정하지 않아도 됩니다.

[Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet을 사용하여 실행 중인 작업의 상태를 확인할 수 있습니다. 지금까지 작업에서 출력을 가져오려면 [Receive-Job ](/powershell/module/microsoft.powershell.core/receive-job) cmdlet을 사용합니다.

Azure에서 원격으로 작업 진행 상황을 확인하려면 작업에서 수정 중인 리소스 형식과 연결된 `Get-` cmdlet을 사용합니다.

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a>참고 항목

* [Azure PowerShell 컨텍스트](context-persistence.md)
* [PowerShell 작업 정보](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [Get-Job 참조](/powershell/module/microsoft.powershell.core/get-job)
* [Receive-Job 참조](/powershell/module/microsoft.powershell.core/receive-job)
