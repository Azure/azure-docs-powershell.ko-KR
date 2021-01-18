---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: 6be8097fb649b6ebdec1c6dc5f28f2a06c572d35
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494574"
---
# Az.Accounts 모듈
## 설명
모든 Azure 모듈에 대한 자격 증명 및 일반 구성을 관리합니다.

## Az.Accounts Cmdlet
### [Add-AzEnvironment](Add-AzEnvironment.md)
Azure Resource Manager의 인스턴스에 대한 엔드포인트 및 메타데이터를 추가합니다.

### [Clear-AzContext](Clear-AzContext.md)
모든 Azure 자격 증명, 계정 및 구독 정보를 제거합니다.

### [Clear-AzDefault](Clear-AzDefault.md)
현재 컨텍스트에서 사용자가 설정한 기본값을 지워야 합니다.

### [Connect-AzAccount](Connect-AzAccount.md)
Az PowerShell 모듈의 cmdlet과 함께 사용하기 위해 인증된 계정으로 Azure에 연결합니다.

### [Disable-AzContextAutosave](Disable-AzContextAutosave.md)
Azure 자격 증명 자동 저장을 해제합니다.  다음에 PowerShell 창을 열면 로그인 정보가 잊혀지기

### [Disable-AzDataCollection](Disable-AzDataCollection.md)
Azure PowerShell cmdlet을 개선하기 위해 데이터 수집을 옵트아웃합니다. 명시적으로 옵트아웃하지 않는 한 기본적으로 데이터가 수집됩니다.

### [Disable-AzureRmAlias](Disable-AzureRmAlias.md)
Az 모듈에 대한 AzureRm 연결부 별칭을 사용하지 않도록 설정합니다.

### [Disconnect-AzAccount](Disconnect-AzAccount.md)
연결된 Azure 계정의 연결을 끊고 해당 계정과 연결된 모든 자격 증명 및 컨텍스트를 제거합니다.

### [Enable-AzContextAutosave](Enable-AzContextAutosave.md)
PowerShell 창을 열 때 Azure 자격 증명, 계정 및 구독 정보를 저장하고 자동으로 로드하도록 허용합니다. 

### [Enable-AzDataCollection](Enable-AzDataCollection.md)
Azure PowerShell cmdlet을 사용하여 사용자 환경을 개선하기 위해 Azure PowerShell에서 데이터를 수집할 수 있습니다. 이 cmdlet을 실행하면 현재 컴퓨터의 현재 사용자에 대한 데이터 수집을 옵트인합니다. 명시적으로 옵트아웃하지 않는 한 기본적으로 데이터가 수집됩니다.

### [Enable-AzureRmAlias](Enable-AzureRmAlias.md)
Az 모듈에 대한 AzureRm 연결부 별칭을 사용할 수 있습니다.

### [Get-AzAccessToken](Get-AzAccessToken.md)
원시 액세스 토큰을 얻습니다.

### [Get-AzContext](Get-AzContext.md)
Azure Resource Manager 요청을 인증하는 데 사용되는 메타데이터를 얻습니다.

### [Get-AzContextAutosaveSetting](Get-AzContextAutosaveSetting.md)
컨텍스트가 자동으로 저장되는지 여부 및 저장된 컨텍스트 및 자격 증명 정보를 찾을 수 있는 위치를 포함하여 컨텍스트 자동 저장 기능에 대한 메타데이터를 표시합니다.

### [Get-AzDefault](Get-AzDefault.md)
현재 컨텍스트에서 사용자가 설정한 기본값을 얻습니다.

### [Get-AzEnvironment](Get-AzEnvironment.md)
Azure 서비스의 인스턴스에 대한 엔드포인트 및 메타데이터를 얻습니다.

### [Get-AzSubscription](Get-AzSubscription.md)
현재 계정이 액세스할 수 있는 구독을 얻습니다.

### [Get-AzTenant](Get-AzTenant.md)
현재 사용자에 대해 권한이 부여된 테넌트를 얻습니다.

### [Import-AzContext](Import-AzContext.md)
파일에서 Azure 인증 정보를 로드합니다.

### [Invoke-AzRestMethod](Invoke-AzRestMethod.md)
Azure 리소스 관리 엔드포인트에만 HTTP 요청을 생성하고 수행

### [Register-AzModule](Register-AzModule.md)
내부 사용 전용 - 생성된 자동Rest cmdlet에 대한 런타임 지원 제공

### [Remove-AzContext](Remove-AzContext.md)
사용 가능한 컨텍스트 집합에서 컨텍스트 제거

### [Remove-AzEnvironment](Remove-AzEnvironment.md)
주어진 Azure 인스턴스에 연결하기 위한 엔드포인트 및 메타데이터를 제거합니다.

### [Rename-AzContext](Rename-AzContext.md)
Azure 컨텍스트의 이름을 변경합니다.  기본적으로 컨텍스트는 사용자 계정 및 구독에 의해 명명됩니다.

### [Resolve-AzError](Resolve-AzError.md)
Azure PowerShell 오류에 대한 확장된 세부 정보와 함께 PowerShell 오류에 대한 자세한 정보를 표시합니다.

### [Save-AzContext](Save-AzContext.md)
다른 PowerShell 세션에서 사용하기 위해 현재 인증 정보를 저장합니다.

### [Select-AzContext](Select-AzContext.md)
Azure PowerShell cmdlet에서 대상으로 할 구독 및 계정 선택

### [피드백 보내기](Send-Feedback.md)
안내된 프롬프트 집합을 통해 Azure PowerShell 팀에 피드백을 전송합니다.

### [Set-AzContext](Set-AzContext.md)
cmdlet이 현재 세션에서 사용할 테넌트, 구독 및 환경을 설정합니다.

### [Set-AzDefault](Set-AzDefault.md)
현재 컨텍스트에서 기본값 설정

### [Set-AzEnvironment](Set-AzEnvironment.md)
Azure 환경에 대한 속성을 지정합니다.

### [Uninstall-AzureRm](Uninstall-AzureRm.md)
컴퓨터에서 모든 AzureRm 모듈을 제거합니다.

