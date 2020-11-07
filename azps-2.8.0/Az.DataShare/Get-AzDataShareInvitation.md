---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: 1f9f0258bf107ae0ca7be7050f8db8e3db8b1ffa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696737"
---
# <span data-ttu-id="2b7f6-101">Get-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="2b7f6-101">Get-AzDataShareInvitation</span></span>

## <span data-ttu-id="2b7f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b7f6-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7f6-103">데이터 공유에 대 한 정보 초대를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-103">Gets information invitation of data share.</span></span>

## <span data-ttu-id="2b7f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b7f6-104">SYNTAX</span></span>

### <span data-ttu-id="2b7f6-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2b7f6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b7f6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b7f6-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b7f6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2b7f6-107">DESCRIPTION</span></span>
<span data-ttu-id="2b7f6-108">**AzDataShareInvitation** cmdlet은 데이터 공유에 추가 된 초대에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-108">The **Get-AzDataShareInvitation** cmdlet gets information on invitations added in data share.</span></span> <span data-ttu-id="2b7f6-109">초대의 이름을 지정 하는 경우이 cmdlet은 초대에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-109">If you specify the name of the invitation, this cmdlet gets information about the invitation.</span></span> <span data-ttu-id="2b7f6-110">이름을 지정 하지 않으면이 cmdlet은 공유의 모든 초대에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-110">If you do not specify a name, this cmdlet gets information about all the invitations in a share.</span></span>

## <span data-ttu-id="2b7f6-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2b7f6-111">EXAMPLES</span></span>

### <span data-ttu-id="2b7f6-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b7f6-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation"

InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="2b7f6-113">이 명령은 adsinvitation 공유에 제공 되는 초대에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-113">This commands provides information about invitation AdsInvitation present in data share AdsShare.</span></span>

## <span data-ttu-id="2b7f6-114">변수</span><span class="sxs-lookup"><span data-stu-id="2b7f6-114">PARAMETERS</span></span>

### <span data-ttu-id="2b7f6-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2b7f6-115">-AccountName</span></span>
<span data-ttu-id="2b7f6-116">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="2b7f6-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7f6-117">-DefaultProfile</span></span>
<span data-ttu-id="2b7f6-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b7f6-119">-이름</span><span class="sxs-lookup"><span data-stu-id="2b7f6-119">-Name</span></span>
<span data-ttu-id="2b7f6-120">Azure data share 초대 이름</span><span class="sxs-lookup"><span data-stu-id="2b7f6-120">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7f6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b7f6-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b7f6-122">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2b7f6-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7f6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b7f6-123">-ResourceId</span></span>
<span data-ttu-id="2b7f6-124">Azure data share 초대의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-124">The resource id of the azure data share invitation</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7f6-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2b7f6-125">-ShareName</span></span>
<span data-ttu-id="2b7f6-126">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="2b7f6-126">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7f6-127">CommonParameters</span></span>
<span data-ttu-id="2b7f6-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7f6-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b7f6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7f6-130">입력</span><span class="sxs-lookup"><span data-stu-id="2b7f6-130">INPUTS</span></span>

### <span data-ttu-id="2b7f6-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2b7f6-131">System.String</span></span>

## <span data-ttu-id="2b7f6-132">출력</span><span class="sxs-lookup"><span data-stu-id="2b7f6-132">OUTPUTS</span></span>

### <span data-ttu-id="2b7f6-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="2b7f6-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="2b7f6-134">상속자</span><span class="sxs-lookup"><span data-stu-id="2b7f6-134">NOTES</span></span>

## <span data-ttu-id="2b7f6-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b7f6-135">RELATED LINKS</span></span>
