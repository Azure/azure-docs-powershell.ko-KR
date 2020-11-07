---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: 885525c568220a6a46c71615a8a18e3682d87d71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696706"
---
# <span data-ttu-id="8b7cd-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="8b7cd-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="8b7cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="8b7cd-103">공유 초대를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="8b7cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b7cd-104">SYNTAX</span></span>

### <span data-ttu-id="8b7cd-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8b7cd-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b7cd-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b7cd-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b7cd-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b7cd-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b7cd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8b7cd-108">DESCRIPTION</span></span>
<span data-ttu-id="8b7cd-109">**AzDataShareInvitation** cmdlet은 공급자 공유에 대 한 정보를 사용 하 여 대상 소비자에 게 초대를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="8b7cd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8b7cd-110">EXAMPLES</span></span>

### <span data-ttu-id="8b7cd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8b7cd-111">Example 1</span></span>
```
PS C:\> New-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation" -TargetEmail "adstest@microsoft.com"
InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/        providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="8b7cd-112">이 명령은 AdsInvitation 초대를 만들어 대상 전자 메일로 보냅니다 adstest@micosoft.com .</span><span class="sxs-lookup"><span data-stu-id="8b7cd-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@micosoft.com.</span></span>

## <span data-ttu-id="8b7cd-113">변수</span><span class="sxs-lookup"><span data-stu-id="8b7cd-113">PARAMETERS</span></span>

### <span data-ttu-id="8b7cd-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8b7cd-114">-AccountName</span></span>
<span data-ttu-id="8b7cd-115">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="8b7cd-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b7cd-116">-DefaultProfile</span></span>
<span data-ttu-id="8b7cd-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b7cd-118">-이름</span><span class="sxs-lookup"><span data-stu-id="8b7cd-118">-Name</span></span>
<span data-ttu-id="8b7cd-119">Azure data share 초대 이름</span><span class="sxs-lookup"><span data-stu-id="8b7cd-119">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b7cd-120">-ResourceGroupName</span></span>
<span data-ttu-id="8b7cd-121">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8b7cd-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-122">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8b7cd-122">-ShareName</span></span>
<span data-ttu-id="8b7cd-123">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="8b7cd-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="8b7cd-124">-TargetEmail</span></span>
<span data-ttu-id="8b7cd-125">대상 전자 메일 id</span><span class="sxs-lookup"><span data-stu-id="8b7cd-125">Target email id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="8b7cd-126">-TargetObjectId</span></span>
<span data-ttu-id="8b7cd-127">대상 개체 id</span><span class="sxs-lookup"><span data-stu-id="8b7cd-127">Target object id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="8b7cd-128">-TargetTenantId</span></span>
<span data-ttu-id="8b7cd-129">대상 테 넌 트 id</span><span class="sxs-lookup"><span data-stu-id="8b7cd-129">Target tenant id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-130">-확인</span><span class="sxs-lookup"><span data-stu-id="8b7cd-130">-Confirm</span></span>
<span data-ttu-id="8b7cd-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b7cd-132">-WhatIf</span></span>
<span data-ttu-id="8b7cd-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b7cd-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b7cd-135">CommonParameters</span></span>
<span data-ttu-id="8b7cd-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b7cd-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b7cd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b7cd-138">입력</span><span class="sxs-lookup"><span data-stu-id="8b7cd-138">INPUTS</span></span>

### <span data-ttu-id="8b7cd-139">않아야</span><span class="sxs-lookup"><span data-stu-id="8b7cd-139">None</span></span>

## <span data-ttu-id="8b7cd-140">출력</span><span class="sxs-lookup"><span data-stu-id="8b7cd-140">OUTPUTS</span></span>

### <span data-ttu-id="8b7cd-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="8b7cd-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="8b7cd-142">상속자</span><span class="sxs-lookup"><span data-stu-id="8b7cd-142">NOTES</span></span>

## <span data-ttu-id="8b7cd-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b7cd-143">RELATED LINKS</span></span>
