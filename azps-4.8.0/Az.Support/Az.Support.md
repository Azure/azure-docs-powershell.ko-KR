---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204703"
---
# Az 지원 모듈
## 설명은
이 섹션의 항목에서는 azure Resource Manager (ARM) 프레임 워크에서 Azure 지원 티켓을 만들고 관리 하기 위한 Azure PowerShell cmdlet을 설명 합니다. 이 cmdlet은 Microsoft Azure. 명령인. 지원 네임 스페이스에 있습니다.

## Az 지원 Cmdlet
### [Get-AzSupportService](Get-AzSupportService.md)
지원을 사용할 수 있는 현재 Azure services 목록을 가져옵니다. 각 Azure 서비스에는 고유한 범주 집합 (문제 분류 라고 함)이 있습니다. Get-AzSupportProblemClassification를 사용 하 여 서비스에 대 한 최신 문제 분류 목록을 가져옵니다. 서비스 및 문제 분류 GUID를 사용 하 여 새 AzSupportTicket를 사용 하 여 새 지원 티켓을 만들 수 있습니다.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Azure 서비스에 대 한 문제 분류의 현재 목록을 가져옵니다. 서비스 및 문제 분류 GUID를 사용 하 여 새 AzSupportTicket를 사용 하 여 새 지원 티켓을 만들 수 있습니다. 

### [새로운 AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
도우미 cmdlet을 통해 지원 연락처 프로필 개체를 만듭니다. New-AzSupportTicket cmdlet에이 개체를 사용할 수 있습니다.

### [새로운 AzSupportTicket](New-AzSupportTicket.md)
새 Azure 지원 티켓을 만듭니다. 이 작업은 Azure [새 지원 요청 페이지](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)의 동작을 모델링 합니다.

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
지원 티켓 목록을 가져옵니다. 티켓 이름에 따라 전체 지원 티켓을 가져오거나 *상태* 또는 *CreatedDate* 지원 티켓을 필터링 할 수 있습니다.

### [업데이트-AzSupportTicket](Update-AzSupportTicket.md)
지원 티켓의 심각도, 상태 또는 고객 연락처 정보를 업데이트 합니다.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
지원 티켓에 대 한 통신을 가져옵니다. *CreatedDate*   또는 *CommunicationType* 에서 지원 티켓 통신을 필터링 할 수도 있습니다. 

### [새로운 AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Azure 지원 티켓에 새 고객 통신을 추가 합니다. 



