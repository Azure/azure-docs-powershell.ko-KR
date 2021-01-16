---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335510"
---
# <span data-ttu-id="d2573-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="d2573-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="d2573-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2573-102">SYNOPSIS</span></span>
<span data-ttu-id="d2573-103">데이터 세트 매핑을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d2573-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="d2573-104">구문</span><span class="sxs-lookup"><span data-stu-id="d2573-104">SYNTAX</span></span>

### <span data-ttu-id="d2573-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d2573-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2573-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2573-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2573-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2573-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2573-108">설명</span><span class="sxs-lookup"><span data-stu-id="d2573-108">DESCRIPTION</span></span>
<span data-ttu-id="d2573-109">**Remove-AzDataShareDataSet** cmdlet은 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d2573-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="d2573-110">예제</span><span class="sxs-lookup"><span data-stu-id="d2573-110">EXAMPLES</span></span>

### <span data-ttu-id="d2573-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d2573-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="d2573-112">이 명령은 공유 WikiAds에서 DS라는 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d2573-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="d2573-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2573-113">PARAMETERS</span></span>

### <span data-ttu-id="d2573-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d2573-114">-AccountName</span></span>
<span data-ttu-id="d2573-115">Azure 데이터 공유 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2573-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="d2573-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2573-116">-DefaultProfile</span></span>
<span data-ttu-id="d2573-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2573-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2573-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2573-118">-InputObject</span></span>
<span data-ttu-id="d2573-119">Azure 데이터 집합 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d2573-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2573-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d2573-120">-Name</span></span>
<span data-ttu-id="d2573-121">Azure 데이터 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2573-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2573-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2573-122">-PassThru</span></span>
<span data-ttu-id="d2573-123">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="d2573-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="d2573-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2573-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2573-125">Azure 데이터 공유 계정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2573-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="d2573-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2573-126">-ResourceId</span></span>
<span data-ttu-id="d2573-127">Azure 데이터 집합의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d2573-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="d2573-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d2573-128">-ShareName</span></span>
<span data-ttu-id="d2573-129">Azure 데이터 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2573-129">Azure data share name.</span></span>

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

### <span data-ttu-id="d2573-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2573-130">-Confirm</span></span>
<span data-ttu-id="d2573-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2573-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2573-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2573-132">-WhatIf</span></span>
<span data-ttu-id="d2573-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d2573-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2573-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2573-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2573-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2573-135">CommonParameters</span></span>
<span data-ttu-id="d2573-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d2573-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2573-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d2573-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2573-138">입력</span><span class="sxs-lookup"><span data-stu-id="d2573-138">INPUTS</span></span>

### <span data-ttu-id="d2573-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d2573-139">System.String</span></span>

### <span data-ttu-id="d2573-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="d2573-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="d2573-141">출력</span><span class="sxs-lookup"><span data-stu-id="d2573-141">OUTPUTS</span></span>

### <span data-ttu-id="d2573-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2573-142">System.Boolean</span></span>

## <span data-ttu-id="d2573-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d2573-143">NOTES</span></span>

## <span data-ttu-id="d2573-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2573-144">RELATED LINKS</span></span>
