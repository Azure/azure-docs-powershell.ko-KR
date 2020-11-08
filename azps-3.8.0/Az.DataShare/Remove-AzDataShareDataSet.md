---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: 1d9566bedbb3e7479f1e9e00c3cc179a225cab2e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042868"
---
# <span data-ttu-id="6c9fd-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="6c9fd-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="6c9fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c9fd-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9fd-103">데이터 집합 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="6c9fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6c9fd-104">SYNTAX</span></span>

### <span data-ttu-id="6c9fd-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6c9fd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c9fd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c9fd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c9fd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c9fd-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c9fd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6c9fd-108">DESCRIPTION</span></span>
<span data-ttu-id="6c9fd-109">**AzDataShareDataSet** cmdlet은 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="6c9fd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6c9fd-110">EXAMPLES</span></span>

### <span data-ttu-id="6c9fd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6c9fd-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="6c9fd-112">이 명령은 share WikiAds에서 DS 라는 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="6c9fd-113">변수</span><span class="sxs-lookup"><span data-stu-id="6c9fd-113">PARAMETERS</span></span>

### <span data-ttu-id="6c9fd-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6c9fd-114">-AccountName</span></span>
<span data-ttu-id="6c9fd-115">Azure data share 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="6c9fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9fd-116">-DefaultProfile</span></span>
<span data-ttu-id="6c9fd-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c9fd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c9fd-118">-InputObject</span></span>
<span data-ttu-id="6c9fd-119">Azure 데이터 집합 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-119">The azure data set object.</span></span>


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

### <span data-ttu-id="6c9fd-120">-이름</span><span class="sxs-lookup"><span data-stu-id="6c9fd-120">-Name</span></span>
<span data-ttu-id="6c9fd-121">Azure 데이터 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-121">Azure data set name.</span></span>

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

### <span data-ttu-id="6c9fd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c9fd-122">-PassThru</span></span>
<span data-ttu-id="6c9fd-123">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="6c9fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c9fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c9fd-125">Azure data share 계정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="6c9fd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c9fd-126">-ResourceId</span></span>
<span data-ttu-id="6c9fd-127">Azure 데이터 집합의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="6c9fd-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="6c9fd-128">-ShareName</span></span>
<span data-ttu-id="6c9fd-129">Azure 데이터 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-129">Azure data share name.</span></span>

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

### <span data-ttu-id="6c9fd-130">-확인</span><span class="sxs-lookup"><span data-stu-id="6c9fd-130">-Confirm</span></span>
<span data-ttu-id="6c9fd-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c9fd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c9fd-132">-WhatIf</span></span>
<span data-ttu-id="6c9fd-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c9fd-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c9fd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9fd-135">CommonParameters</span></span>
<span data-ttu-id="6c9fd-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c9fd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9fd-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c9fd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9fd-138">입력</span><span class="sxs-lookup"><span data-stu-id="6c9fd-138">INPUTS</span></span>

### <span data-ttu-id="6c9fd-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6c9fd-139">System.String</span></span>

### <span data-ttu-id="6c9fd-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="6c9fd-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="6c9fd-141">출력</span><span class="sxs-lookup"><span data-stu-id="6c9fd-141">OUTPUTS</span></span>

### <span data-ttu-id="6c9fd-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6c9fd-142">System.Boolean</span></span>

## <span data-ttu-id="6c9fd-143">상속자</span><span class="sxs-lookup"><span data-stu-id="6c9fd-143">NOTES</span></span>

## <span data-ttu-id="6c9fd-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c9fd-144">RELATED LINKS</span></span>
