---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377126"
---
# <span data-ttu-id="faff7-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="faff7-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="faff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faff7-102">SYNOPSIS</span></span>
<span data-ttu-id="faff7-103">데이터 세트 매핑을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="faff7-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="faff7-104">구문</span><span class="sxs-lookup"><span data-stu-id="faff7-104">SYNTAX</span></span>

### <span data-ttu-id="faff7-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="faff7-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faff7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="faff7-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faff7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="faff7-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faff7-108">설명</span><span class="sxs-lookup"><span data-stu-id="faff7-108">DESCRIPTION</span></span>
<span data-ttu-id="faff7-109">**Remove-AzDataShareDataSetMapping** cmdlet은 데이터 세트 매핑을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="faff7-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="faff7-110">예제</span><span class="sxs-lookup"><span data-stu-id="faff7-110">EXAMPLES</span></span>

### <span data-ttu-id="faff7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="faff7-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="faff7-112">이 명령은 sharesubscription WikiAds에서 DSM이라는 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="faff7-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="faff7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="faff7-113">PARAMETERS</span></span>

### <span data-ttu-id="faff7-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="faff7-114">-AccountName</span></span>
<span data-ttu-id="faff7-115">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="faff7-115">Azure data share account name</span></span>

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

### <span data-ttu-id="faff7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faff7-116">-DefaultProfile</span></span>
<span data-ttu-id="faff7-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="faff7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faff7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="faff7-118">-InputObject</span></span>
<span data-ttu-id="faff7-119">Azure 데이터 집합 매핑 개체</span><span class="sxs-lookup"><span data-stu-id="faff7-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="faff7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="faff7-120">-Name</span></span>
<span data-ttu-id="faff7-121">Azure 데이터 집합 매핑 이름</span><span class="sxs-lookup"><span data-stu-id="faff7-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="faff7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="faff7-122">-PassThru</span></span>
<span data-ttu-id="faff7-123">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="faff7-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="faff7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faff7-124">-ResourceGroupName</span></span>
<span data-ttu-id="faff7-125">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="faff7-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="faff7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="faff7-126">-ResourceId</span></span>
<span data-ttu-id="faff7-127">Azure 데이터 집합 매핑의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="faff7-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="faff7-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="faff7-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="faff7-129">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="faff7-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="faff7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="faff7-130">-Confirm</span></span>
<span data-ttu-id="faff7-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="faff7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faff7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faff7-132">-WhatIf</span></span>
<span data-ttu-id="faff7-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="faff7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faff7-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="faff7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faff7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faff7-135">CommonParameters</span></span>
<span data-ttu-id="faff7-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="faff7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faff7-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="faff7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faff7-138">입력</span><span class="sxs-lookup"><span data-stu-id="faff7-138">INPUTS</span></span>

### <span data-ttu-id="faff7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="faff7-139">System.String</span></span>

### <span data-ttu-id="faff7-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="faff7-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="faff7-141">출력</span><span class="sxs-lookup"><span data-stu-id="faff7-141">OUTPUTS</span></span>

### <span data-ttu-id="faff7-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="faff7-142">System.Boolean</span></span>

## <span data-ttu-id="faff7-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="faff7-143">NOTES</span></span>

## <span data-ttu-id="faff7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="faff7-144">RELATED LINKS</span></span>
