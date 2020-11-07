---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: c0f8ea29a795b7b88a6e79134d52c3dd00ad5f42
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875230"
---
# Az 모듈
## 설명은
모든 Azure 모듈에 대 한 자격 증명과 공통 구성을 관리 합니다.

## Az Cmdlet
### [추가-AzEnvironment](Add-AzEnvironment.md)
Azure Resource Manager 인스턴스에 대 한 끝점 및 메타 데이터를 추가 합니다.

### [일반-AzContext](Clear-AzContext.md)
모든 Azure 자격 증명, 계정 및 구독 정보를 제거 합니다.

### [일반-AzDefault](Clear-AzDefault.md)
현재 컨텍스트에서 사용자가 설정한 기본값을 지웁니다.

### [연결-AzAccount](Connect-AzAccount.md)
Azure Resource Manager cmdlet 요청과 함께 사용할 인증 된 계정으로 Azure에 연결 합니다.

### [Disable-AzContextAutosave](Disable-AzContextAutosave.md)
Autosaving Azure 자격 증명을 끄십시오.  다음에 PowerShell 창을 열 때 로그인 정보가 기억나지 않습니다.

### [Disable-AzDataCollection](Disable-AzDataCollection.md)
Opts에서 데이터를 수집 하 여 AzurePowerShell cmdlet을 개선 했습니다. 명시적으로 옵트인 하지 않는 한 데이터는 수집 되지 않습니다.

### [Disable-AzureRmAlias](Disable-AzureRmAlias.md)
Az 모듈에 AzureRm 접두사 별칭을 사용 하지 않도록 설정 합니다.

### [연결 해제-AzAccount](Disconnect-AzAccount.md)
연결 된 Azure 계정의 연결을 끊고 해당 계정과 관련 된 모든 자격 증명과 컨텍스트를 제거 합니다.

### [Enable-AzContextAutosave](Enable-AzContextAutosave.md)
Azure 자격 증명, 계정, 구독 정보를 저장 하 고 PowerShell 창을 열 때 자동으로 로드 하도록 허용 합니다. 

### [Enable-AzDataCollection](Enable-AzDataCollection.md)
Azure PowerShell에서 데이터를 수집 하 여 AzurePowerShell cmdlet을 사용 하 여 사용자 환경을 향상 시킬 수 있습니다.
현재 컴퓨터의 현재 사용자에 대 한 데이터 수집에 opts cmdlet을 실행 합니다.
명시적으로 옵트인 하지 않는 한 데이터는 수집 되지 않습니다.

### [Enable-AzureRmAlias](Enable-AzureRmAlias.md)
Az 모듈에 대 한 AzureRm 접두사 별칭을 사용 하도록 설정 합니다.

### [Get-AzContext](Get-AzContext.md)
Azure Resource Manager 요청을 인증 하는 데 사용 되는 메타 데이터를 가져옵니다.

### [Get-AzContextAutosaveSetting](Get-AzContextAutosaveSetting.md)
컨텍스트가 자동으로 저장 되는지 여부와 저장 된 컨텍스트 및 자격 증명 정보를 찾을 수 있는 위치를 포함 하 여 컨텍스트 자동 저장 기능에 대 한 메타 데이터를 표시 합니다.

### [Get-AzDefault](Get-AzDefault.md)
사용자가 현재 컨텍스트에서 설정한 기본값을 가져옵니다.

### [Get-AzEnvironment](Get-AzEnvironment.md)
Azure services 인스턴스에 대 한 끝점 및 메타 데이터를 가져옵니다.

### [Get-AzProfile](Get-AzProfile.md)
설치 된 모듈에서 지원 되는 서비스 프로필을 가져옵니다.

### [Get-AzSubscription](Get-AzSubscription.md)
현재 계정이 액세스할 수 있는 구독을 가져옵니다.

### [Get-AzTenant](Get-AzTenant.md)
현재 사용자에 대해 권한이 있는 테 넌 트를 가져옵니다.

### [가져오기-AzContext](Import-AzContext.md)
파일에서 Azure 인증 정보를 로드 합니다.

### [Register-AzModule](Register-AzModule.md)
내부용 전용-AutoRest 생성 된 cmdlet에 대 한 런타임 지원을 제공 합니다.

### [제거-AzContext](Remove-AzContext.md)
사용 가능한 컨텍스트 집합에서 컨텍스트 제거

### [제거-AzEnvironment](Remove-AzEnvironment.md)
지정 된 Azure 인스턴스에 연결 하기 위한 끝점 및 메타 데이터를 제거 합니다.

### [이름 바꾸기-AzContext](Rename-AzContext.md)
Azure 컨텍스트의 이름을 바꿉니다.  기본적으로 컨텍스트는 사용자 계정과 구독으로 명명 됩니다.

### [해결-AzError](Resolve-AzError.md)
Azure PowerShell 오류에 대 한 자세한 세부 정보를 포함 하 여 PowerShell 오류에 대 한 자세한 정보를 표시 합니다.

### [저장-AzContext](Save-AzContext.md)
다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.

### [선택-AzContext](Select-AzContext.md)
Azure PowerShell cmdlet에서 대상 구독 및 계정 선택

### [선택-AzProfile](Select-AzProfile.md)
여러 서비스 프로필을 지 원하는 모듈의 경우 지정 된 서비스 프로필에 해당 하는 cmdlet을 로드 합니다.

### [보내기-피드백](Send-Feedback.md)
안내 표시를 통해 Azure PowerShell 팀에 의견을 보냅니다.

### [Set-AzContext](Set-AzContext.md)
Cmdlet에 대 한 테 넌 트, 구독 및 환경을 현재 세션에서 사용할 수 있도록 설정 합니다.

### [Set-AzDefault](Set-AzDefault.md)
현재 컨텍스트에서 기본값을 설정 합니다.

### [Set-AzEnvironment](Set-AzEnvironment.md)
Azure 환경에 대 한 속성을 설정 합니다.

### [제거-AzureRm](Uninstall-AzureRm.md)
컴퓨터에서 모든 AzureRm 모듈을 제거 합니다.

