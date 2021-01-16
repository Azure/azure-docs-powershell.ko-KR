---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377147"
---
# <span data-ttu-id="a9c65-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="a9c65-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="a9c65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9c65-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c65-103">데이터 세트 매핑을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9c65-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="a9c65-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9c65-104">SYNTAX</span></span>

### <span data-ttu-id="a9c65-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a9c65-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9c65-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9c65-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9c65-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9c65-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9c65-108">설명</span><span class="sxs-lookup"><span data-stu-id="a9c65-108">DESCRIPTION</span></span>
<span data-ttu-id="a9c65-109">**Remove-AzDataShareDataSet** cmdlet은 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9c65-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="a9c65-110">예제</span><span class="sxs-lookup"><span data-stu-id="a9c65-110">EXAMPLES</span></span>

### <span data-ttu-id="a9c65-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a9c65-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="a9c65-112">이 명령은 공유 WikiAds에서 DS라는 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9c65-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="a9c65-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9c65-113">PARAMETERS</span></span>

### <span data-ttu-id="a9c65-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a9c65-114">-AccountName</span></span>
<span data-ttu-id="a9c65-115">Azure 데이터 공유 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9c65-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="a9c65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c65-116">-DefaultProfile</span></span>
<span data-ttu-id="a9c65-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9c65-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9c65-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9c65-118">-InputObject</span></span>
<span data-ttu-id="a9c65-119">Azure 데이터 집합 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a9c65-119">The azure data set object.</span></span>


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

### <span data-ttu-id="a9c65-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a9c65-120">-Name</span></span>
<span data-ttu-id="a9c65-121">Azure 데이터 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9c65-121">Azure data set name.</span></span>

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

### <span data-ttu-id="a9c65-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9c65-122">-PassThru</span></span>
<span data-ttu-id="a9c65-123">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="a9c65-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="a9c65-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c65-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9c65-125">Azure 데이터 공유 계정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9c65-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="a9c65-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9c65-126">-ResourceId</span></span>
<span data-ttu-id="a9c65-127">Azure 데이터 집합의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a9c65-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="a9c65-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a9c65-128">-ShareName</span></span>
<span data-ttu-id="a9c65-129">Azure 데이터 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9c65-129">Azure data share name.</span></span>

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

### <span data-ttu-id="a9c65-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9c65-130">-Confirm</span></span>
<span data-ttu-id="a9c65-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9c65-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9c65-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9c65-132">-WhatIf</span></span>
<span data-ttu-id="a9c65-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a9c65-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9c65-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9c65-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9c65-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c65-135">CommonParameters</span></span>
<span data-ttu-id="a9c65-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9c65-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c65-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9c65-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c65-138">입력</span><span class="sxs-lookup"><span data-stu-id="a9c65-138">INPUTS</span></span>

### <span data-ttu-id="a9c65-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a9c65-139">System.String</span></span>

### <span data-ttu-id="a9c65-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="a9c65-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="a9c65-141">출력</span><span class="sxs-lookup"><span data-stu-id="a9c65-141">OUTPUTS</span></span>

### <span data-ttu-id="a9c65-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9c65-142">System.Boolean</span></span>

## <span data-ttu-id="a9c65-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9c65-143">NOTES</span></span>

## <span data-ttu-id="a9c65-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9c65-144">RELATED LINKS</span></span>
