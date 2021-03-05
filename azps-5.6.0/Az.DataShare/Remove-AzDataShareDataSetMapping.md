---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 8e3513621b94a7fc98a00b7eb443bef18d2a8141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988232"
---
# <span data-ttu-id="2b68f-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="2b68f-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="2b68f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b68f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b68f-103">데이터 세트 매핑 제거</span><span class="sxs-lookup"><span data-stu-id="2b68f-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="2b68f-104">구문</span><span class="sxs-lookup"><span data-stu-id="2b68f-104">SYNTAX</span></span>

### <span data-ttu-id="2b68f-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2b68f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b68f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b68f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b68f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b68f-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b68f-108">설명</span><span class="sxs-lookup"><span data-stu-id="2b68f-108">DESCRIPTION</span></span>
<span data-ttu-id="2b68f-109">**Remove-AzDataShareDataSetMapping** cmdlet은 데이터 세트 매핑을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2b68f-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="2b68f-110">예제</span><span class="sxs-lookup"><span data-stu-id="2b68f-110">EXAMPLES</span></span>

### <span data-ttu-id="2b68f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b68f-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="2b68f-112">이 명령은 sharesubscription WikiAds에서 DSM이라는 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2b68f-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="2b68f-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2b68f-113">PARAMETERS</span></span>

### <span data-ttu-id="2b68f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2b68f-114">-AccountName</span></span>
<span data-ttu-id="2b68f-115">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="2b68f-115">Azure data share account name</span></span>

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

### <span data-ttu-id="2b68f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b68f-116">-DefaultProfile</span></span>
<span data-ttu-id="2b68f-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b68f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b68f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b68f-118">-InputObject</span></span>
<span data-ttu-id="2b68f-119">Azure 데이터 세트 매핑 개체</span><span class="sxs-lookup"><span data-stu-id="2b68f-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b68f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2b68f-120">-Name</span></span>
<span data-ttu-id="2b68f-121">Azure 데이터 세트 매핑 이름</span><span class="sxs-lookup"><span data-stu-id="2b68f-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="2b68f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b68f-122">-PassThru</span></span>
<span data-ttu-id="2b68f-123">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="2b68f-123">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b68f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b68f-124">-ResourceGroupName</span></span>
<span data-ttu-id="2b68f-125">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2b68f-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2b68f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b68f-126">-ResourceId</span></span>
<span data-ttu-id="2b68f-127">Azure 데이터 집합 매핑의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="2b68f-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="2b68f-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2b68f-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="2b68f-129">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="2b68f-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="2b68f-130">-확인</span><span class="sxs-lookup"><span data-stu-id="2b68f-130">-Confirm</span></span>
<span data-ttu-id="2b68f-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b68f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b68f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b68f-132">-WhatIf</span></span>
<span data-ttu-id="2b68f-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2b68f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b68f-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b68f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b68f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b68f-135">CommonParameters</span></span>
<span data-ttu-id="2b68f-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2b68f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b68f-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b68f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b68f-138">입력</span><span class="sxs-lookup"><span data-stu-id="2b68f-138">INPUTS</span></span>

### <span data-ttu-id="2b68f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2b68f-139">System.String</span></span>

### <span data-ttu-id="2b68f-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="2b68f-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="2b68f-141">출력</span><span class="sxs-lookup"><span data-stu-id="2b68f-141">OUTPUTS</span></span>

### <span data-ttu-id="2b68f-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2b68f-142">System.Boolean</span></span>

## <span data-ttu-id="2b68f-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2b68f-143">NOTES</span></span>

## <span data-ttu-id="2b68f-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b68f-144">RELATED LINKS</span></span>
