---
Module Name: AzureRM.Profile
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
ms.openlocfilehash: b9aa5f188d2c4c0167068d304487a0a7d4c7ea2d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522791"
---
# AzureRM 모듈
## 설명은
모든 Azure 모듈에 대 한 자격 증명과 공통 구성을 관리 합니다.

## AzureRM Cmdlet
### [추가-AzureRmEnvironment](Add-AzureRmEnvironment.md)
Azure Resource Manager 인스턴스에 대 한 끝점 및 메타 데이터를 추가 합니다.

### [일반-AzureRmContext](Clear-AzureRmContext.md)
모든 Azure 자격 증명, 계정 및 구독 정보를 제거 합니다.

### [일반-AzureRmDefault](Clear-AzureRmDefault.md)
현재 컨텍스트에서 사용자가 설정한 기본값을 지웁니다.

### [연결-AzureRmAccount](Connect-AzureRmAccount.md)
Azure Resource Manager cmdlet 요청과 함께 사용할 인증 된 계정으로 Azure에 연결 합니다.

### [Disable-AzureRmContextAutosave](Disable-AzureRmContextAutosave.md)
Autosaving Azure 자격 증명을 끄십시오.  다음에 PowerShell 창을 열 때 로그인 정보가 기억나지 않습니다.

### [Disable-AzureRmDataCollection](Disable-AzureRmDataCollection.md)
Opts에서 데이터를 수집 하 여 AzurePowerShell cmdlet을 개선 했습니다. 명시적으로 옵트인 하지 않는 한 데이터는 수집 되지 않습니다.

### [연결 해제-AzureRmAccount](Disconnect-AzureRmAccount.md)
연결 된 Azure 계정의 연결을 끊고 해당 계정과 관련 된 모든 자격 증명과 컨텍스트를 제거 합니다.

### [Enable-AzureRmContextAutosave](Enable-AzureRmContextAutosave.md)
Azure 자격 증명, 계정, 구독 정보를 저장 하 고 PowerShell 창을 열 때 자동으로 로드 하도록 허용 합니다. 

### [Enable-AzureRmDataCollection](Enable-AzureRmDataCollection.md)
Azure PowerShell에서 데이터를 수집 하 여 AzurePowerShell cmdlet을 사용 하 여 사용자 환경을 향상 시킬 수 있습니다.
현재 컴퓨터의 현재 사용자에 대 한 데이터 수집에 opts cmdlet을 실행 합니다.
명시적으로 옵트인 하지 않는 한 데이터는 수집 되지 않습니다.

### [Get-AzureRmContext](Get-AzureRmContext.md)
Azure Resource Manager 요청을 인증 하는 데 사용 되는 메타 데이터를 가져옵니다.

### [Get-AzureRmContextAutosaveSetting](Get-AzureRmContextAutosaveSetting.md)
컨텍스트가 자동으로 저장 되는지 여부와 저장 된 컨텍스트 및 자격 증명 정보를 찾을 수 있는 위치를 포함 하 여 컨텍스트 자동 저장 기능에 대 한 메타 데이터를 표시 합니다.

### [Get-AzureRmDefault](Get-AzureRmDefault.md)
사용자가 현재 컨텍스트에서 설정한 기본값을 가져옵니다.

### [Get-AzureRmEnvironment](Get-AzureRmEnvironment.md)
Azure services 인스턴스에 대 한 끝점 및 메타 데이터를 가져옵니다.

### [Get-AzureRmSubscription](Get-AzureRmSubscription.md)
현재 계정이 액세스할 수 있는 구독을 가져옵니다.

### [Get-AzureRmTenant](Get-AzureRmTenant.md)
현재 사용자에 대해 권한이 있는 테 넌 트를 가져옵니다.

### [가져오기-AzureRmContext](Import-AzureRmContext.md)
파일에서 Azure 인증 정보를 로드 합니다.

### [제거-AzureRmContext](Remove-AzureRmContext.md)
사용 가능한 컨텍스트 집합에서 컨텍스트 제거

### [제거-AzureRmEnvironment](Remove-AzureRmEnvironment.md)
지정 된 Azure 인스턴스에 연결 하기 위한 끝점 및 메타 데이터를 제거 합니다.

### [이름 바꾸기-AzureRmContext](Rename-AzureRmContext.md)
Azure 컨텍스트의 이름을 바꿉니다.  기본적으로 컨텍스트는 사용자 계정과 구독으로 명명 됩니다.

### [해결-AzureRmError](Resolve-AzureRmError.md)
Azure PowerShell 오류에 대 한 자세한 세부 정보를 포함 하 여 PowerShell 오류에 대 한 자세한 정보를 표시 합니다.

### [저장-AzureRmContext](Save-AzureRmContext.md)
다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.

### [선택-AzureRmContext](Select-AzureRmContext.md)
Azure PowerShell cmdlet에서 대상 구독 및 계정 선택

### [보내기-피드백](Send-Feedback.md)
안내 표시를 통해 Azure PowerShell 팀에 의견을 보냅니다.

### [Set-AzureRmContext](Set-AzureRmContext.md)
Cmdlet에 대 한 테 넌 트, 구독 및 환경을 현재 세션에서 사용할 수 있도록 설정 합니다.

### [Set-AzureRmDefault](Set-AzureRmDefault.md)
현재 컨텍스트에서 기본값을 설정 합니다.

### [Set-AzureRmEnvironment](Set-AzureRmEnvironment.md)
Azure 환경에 대 한 속성을 설정 합니다.

