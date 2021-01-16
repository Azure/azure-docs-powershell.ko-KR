---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 939b50f6725497bb28ea333f13c04c6281f34611
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372303"
---
# <span data-ttu-id="36bdf-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="36bdf-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="36bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="36bdf-103">소비자 초대에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36bdf-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="36bdf-104">구문</span><span class="sxs-lookup"><span data-stu-id="36bdf-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36bdf-105">설명</span><span class="sxs-lookup"><span data-stu-id="36bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="36bdf-106">**Get-AzDataShareReceivedInvitation** cmdlet은 소비자가 인식한 모든 초대에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="36bdf-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="36bdf-107">위치 또는 초대 ID를 제공하는 경우 이 cmdlet은 특정 위치 또는 초대 ID가 있는 초대에 대한 정보를 제공합니다. 그렇지 않으면 소비자에게 전송된 초대 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="36bdf-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="36bdf-108">예제</span><span class="sxs-lookup"><span data-stu-id="36bdf-108">EXAMPLES</span></span>

### <span data-ttu-id="36bdf-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="36bdf-109">Example 1</span></span>
```
PS C:\> Get-AzDataShareReceivedInvitation -location "westus"

DataSetCount      : 3
InvitationId      : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus  : Pending
Location          : westus
RespondedAt       :
Sender            : adsprovider@microsoft.com
SenderCompanyName : ADS Test
SentAt            : 7/8/2019 10:47:10 PM
ShareName         : AdsShare
Description       : Some description
Terms             : Some terms of use
Id                : /providers/Microsoft.DataShare/consumerInvitations/167e06ff-567f-4bc7-be0c-645a6de710f3
Name              : AdsInvitation
Type              : Microsoft.DataShare/consumerInvitations
```

<span data-ttu-id="36bdf-110">이 Commant는 소비자 초대에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="36bdf-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="36bdf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36bdf-111">PARAMETERS</span></span>

### <span data-ttu-id="36bdf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36bdf-112">-DefaultProfile</span></span>
<span data-ttu-id="36bdf-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36bdf-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bdf-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="36bdf-114">-InvitationId</span></span>
<span data-ttu-id="36bdf-115">Azure dataShare 초대 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="36bdf-115">Azure dataShare invitation id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bdf-116">-Location</span><span class="sxs-lookup"><span data-stu-id="36bdf-116">-Location</span></span>
<span data-ttu-id="36bdf-117">Azure 데이터 공유 초대 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="36bdf-117">Azure data share invitation location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bdf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36bdf-118">CommonParameters</span></span>
<span data-ttu-id="36bdf-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36bdf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36bdf-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36bdf-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36bdf-121">입력</span><span class="sxs-lookup"><span data-stu-id="36bdf-121">INPUTS</span></span>

### <span data-ttu-id="36bdf-122">없음</span><span class="sxs-lookup"><span data-stu-id="36bdf-122">None</span></span>

## <span data-ttu-id="36bdf-123">출력</span><span class="sxs-lookup"><span data-stu-id="36bdf-123">OUTPUTS</span></span>

### <span data-ttu-id="36bdf-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="36bdf-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="36bdf-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36bdf-125">NOTES</span></span>

## <span data-ttu-id="36bdf-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36bdf-126">RELATED LINKS</span></span>
