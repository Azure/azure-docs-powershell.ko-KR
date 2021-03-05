---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: a27989a1637443335389ba8b35bd90279a8976f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996725"
---
# <span data-ttu-id="bf484-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="bf484-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="bf484-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf484-102">SYNOPSIS</span></span>
<span data-ttu-id="bf484-103">공유에 대한 초대를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf484-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="bf484-104">구문</span><span class="sxs-lookup"><span data-stu-id="bf484-104">SYNTAX</span></span>

### <span data-ttu-id="bf484-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bf484-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf484-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf484-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf484-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf484-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf484-108">설명</span><span class="sxs-lookup"><span data-stu-id="bf484-108">DESCRIPTION</span></span>
<span data-ttu-id="bf484-109">**New-AzDataShareInvitation** cmdlet은 공급자 공유에 대한 정보를 통해 대상 소비자에게 초대를 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="bf484-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="bf484-110">예제</span><span class="sxs-lookup"><span data-stu-id="bf484-110">EXAMPLES</span></span>

### <span data-ttu-id="bf484-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bf484-111">Example 1</span></span>
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

<span data-ttu-id="bf484-112">이 명령은 Share AdsShare에 대한 초대 AdsInvitation을 만들고 대상 전자 메일로 adstest@microsoft.com 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="bf484-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="bf484-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bf484-113">PARAMETERS</span></span>

### <span data-ttu-id="bf484-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bf484-114">-AccountName</span></span>
<span data-ttu-id="bf484-115">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="bf484-115">Azure data share account name</span></span>

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

### <span data-ttu-id="bf484-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf484-116">-DefaultProfile</span></span>
<span data-ttu-id="bf484-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf484-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf484-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bf484-118">-Name</span></span>
<span data-ttu-id="bf484-119">Azure 데이터 공유 초대 이름</span><span class="sxs-lookup"><span data-stu-id="bf484-119">Azure data share invitation name</span></span>

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

### <span data-ttu-id="bf484-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf484-120">-ResourceGroupName</span></span>
<span data-ttu-id="bf484-121">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bf484-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="bf484-122">-ShareName</span><span class="sxs-lookup"><span data-stu-id="bf484-122">-ShareName</span></span>
<span data-ttu-id="bf484-123">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="bf484-123">Azure data share name</span></span>

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

### <span data-ttu-id="bf484-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="bf484-124">-TargetEmail</span></span>
<span data-ttu-id="bf484-125">대상 전자 메일 ID</span><span class="sxs-lookup"><span data-stu-id="bf484-125">Target email id</span></span>

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

### <span data-ttu-id="bf484-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="bf484-126">-TargetObjectId</span></span>
<span data-ttu-id="bf484-127">대상 개체 ID</span><span class="sxs-lookup"><span data-stu-id="bf484-127">Target object id</span></span>

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

### <span data-ttu-id="bf484-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="bf484-128">-TargetTenantId</span></span>
<span data-ttu-id="bf484-129">대상 테넌트 ID</span><span class="sxs-lookup"><span data-stu-id="bf484-129">Target tenant id</span></span>

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

### <span data-ttu-id="bf484-130">-확인</span><span class="sxs-lookup"><span data-stu-id="bf484-130">-Confirm</span></span>
<span data-ttu-id="bf484-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf484-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf484-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf484-132">-WhatIf</span></span>
<span data-ttu-id="bf484-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf484-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf484-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf484-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf484-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf484-135">CommonParameters</span></span>
<span data-ttu-id="bf484-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bf484-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf484-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf484-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf484-138">입력</span><span class="sxs-lookup"><span data-stu-id="bf484-138">INPUTS</span></span>

### <span data-ttu-id="bf484-139">없음</span><span class="sxs-lookup"><span data-stu-id="bf484-139">None</span></span>

## <span data-ttu-id="bf484-140">출력</span><span class="sxs-lookup"><span data-stu-id="bf484-140">OUTPUTS</span></span>

### <span data-ttu-id="bf484-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="bf484-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="bf484-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bf484-142">NOTES</span></span>

## <span data-ttu-id="bf484-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf484-143">RELATED LINKS</span></span>
