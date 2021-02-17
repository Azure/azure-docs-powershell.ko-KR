---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: ea042cb0db8fcb1995a935086d188efbb6c0647f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198788"
---
# <span data-ttu-id="01629-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="01629-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="01629-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01629-102">SYNOPSIS</span></span>
<span data-ttu-id="01629-103">공유를 위한 초대를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01629-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="01629-104">구문</span><span class="sxs-lookup"><span data-stu-id="01629-104">SYNTAX</span></span>

### <span data-ttu-id="01629-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="01629-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01629-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="01629-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01629-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="01629-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01629-108">설명</span><span class="sxs-lookup"><span data-stu-id="01629-108">DESCRIPTION</span></span>
<span data-ttu-id="01629-109">**New-AzDataShareInvitation** cmdlet은 공급자 공유에 대한 정보와 함께 대상 소비자에게 초대를 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="01629-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="01629-110">예제</span><span class="sxs-lookup"><span data-stu-id="01629-110">EXAMPLES</span></span>

### <span data-ttu-id="01629-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="01629-111">Example 1</span></span>
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

<span data-ttu-id="01629-112">이 명령은 공유 AdsShare에 대한 AdsInvitation 초대를 만들고 대상 전자 메일로 adstest@microsoft.com 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="01629-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="01629-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01629-113">PARAMETERS</span></span>

### <span data-ttu-id="01629-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="01629-114">-AccountName</span></span>
<span data-ttu-id="01629-115">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="01629-115">Azure data share account name</span></span>

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

### <span data-ttu-id="01629-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01629-116">-DefaultProfile</span></span>
<span data-ttu-id="01629-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01629-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01629-118">-Name</span><span class="sxs-lookup"><span data-stu-id="01629-118">-Name</span></span>
<span data-ttu-id="01629-119">Azure 데이터 공유 초대 이름</span><span class="sxs-lookup"><span data-stu-id="01629-119">Azure data share invitation name</span></span>

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

### <span data-ttu-id="01629-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01629-120">-ResourceGroupName</span></span>
<span data-ttu-id="01629-121">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="01629-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="01629-122">-ShareName</span><span class="sxs-lookup"><span data-stu-id="01629-122">-ShareName</span></span>
<span data-ttu-id="01629-123">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="01629-123">Azure data share name</span></span>

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

### <span data-ttu-id="01629-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="01629-124">-TargetEmail</span></span>
<span data-ttu-id="01629-125">대상 전자 메일 ID</span><span class="sxs-lookup"><span data-stu-id="01629-125">Target email id</span></span>

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

### <span data-ttu-id="01629-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="01629-126">-TargetObjectId</span></span>
<span data-ttu-id="01629-127">대상 개체 ID</span><span class="sxs-lookup"><span data-stu-id="01629-127">Target object id</span></span>

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

### <span data-ttu-id="01629-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="01629-128">-TargetTenantId</span></span>
<span data-ttu-id="01629-129">대상 테넌트 ID</span><span class="sxs-lookup"><span data-stu-id="01629-129">Target tenant id</span></span>

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

### <span data-ttu-id="01629-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01629-130">-Confirm</span></span>
<span data-ttu-id="01629-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="01629-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01629-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01629-132">-WhatIf</span></span>
<span data-ttu-id="01629-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="01629-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01629-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01629-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01629-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01629-135">CommonParameters</span></span>
<span data-ttu-id="01629-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="01629-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01629-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01629-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01629-138">입력</span><span class="sxs-lookup"><span data-stu-id="01629-138">INPUTS</span></span>

### <span data-ttu-id="01629-139">없음</span><span class="sxs-lookup"><span data-stu-id="01629-139">None</span></span>

## <span data-ttu-id="01629-140">출력</span><span class="sxs-lookup"><span data-stu-id="01629-140">OUTPUTS</span></span>

### <span data-ttu-id="01629-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="01629-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="01629-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="01629-142">NOTES</span></span>

## <span data-ttu-id="01629-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01629-143">RELATED LINKS</span></span>
