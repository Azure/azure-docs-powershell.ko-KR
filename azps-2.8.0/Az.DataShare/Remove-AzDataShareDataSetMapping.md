---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 249f166bcf4dd61d9b8da7cf4d67a2ac20f705ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696692"
---
# <span data-ttu-id="a0ca0-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="a0ca0-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="a0ca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ca0-103">데이터 집합 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ca0-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="a0ca0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0ca0-104">SYNTAX</span></span>

### <span data-ttu-id="a0ca0-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a0ca0-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0ca0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0ca0-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0ca0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0ca0-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0ca0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a0ca0-108">DESCRIPTION</span></span>
<span data-ttu-id="a0ca0-109">**AzDataShareDataSetMapping** cmdlet은 데이터 집합 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ca0-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="a0ca0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a0ca0-110">EXAMPLES</span></span>

### <span data-ttu-id="a0ca0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a0ca0-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="a0ca0-112">이 명령은 sharesubscription WikiAds에서 DSM 이라는 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ca0-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="a0ca0-113">변수</span><span class="sxs-lookup"><span data-stu-id="a0ca0-113">PARAMETERS</span></span>

### <span data-ttu-id="a0ca0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a0ca0-114">-AccountName</span></span>
<span data-ttu-id="a0ca0-115">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="a0ca0-115">Azure data share account name</span></span>

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

### <span data-ttu-id="a0ca0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ca0-116">-DefaultProfile</span></span>
<span data-ttu-id="a0ca0-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0ca0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0ca0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0ca0-118">-InputObject</span></span>
<span data-ttu-id="a0ca0-119">Azure 데이터 집합 매핑 개체</span><span class="sxs-lookup"><span data-stu-id="a0ca0-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="a0ca0-120">-이름</span><span class="sxs-lookup"><span data-stu-id="a0ca0-120">-Name</span></span>
<span data-ttu-id="a0ca0-121">Azure 데이터 집합 매핑 이름</span><span class="sxs-lookup"><span data-stu-id="a0ca0-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="a0ca0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0ca0-122">-PassThru</span></span>
<span data-ttu-id="a0ca0-123">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ca0-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="a0ca0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ca0-124">-ResourceGroupName</span></span>
<span data-ttu-id="a0ca0-125">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a0ca0-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a0ca0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0ca0-126">-ResourceId</span></span>
<span data-ttu-id="a0ca0-127">Azure 데이터 집합 매핑의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="a0ca0-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="a0ca0-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a0ca0-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="a0ca0-129">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="a0ca0-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="a0ca0-130">-확인</span><span class="sxs-lookup"><span data-stu-id="a0ca0-130">-Confirm</span></span>
<span data-ttu-id="a0ca0-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ca0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0ca0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0ca0-132">-WhatIf</span></span>
<span data-ttu-id="a0ca0-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0ca0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0ca0-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0ca0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0ca0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ca0-135">CommonParameters</span></span>
<span data-ttu-id="a0ca0-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ca0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ca0-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0ca0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ca0-138">입력</span><span class="sxs-lookup"><span data-stu-id="a0ca0-138">INPUTS</span></span>

### <span data-ttu-id="a0ca0-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a0ca0-139">System.String</span></span>

### <span data-ttu-id="a0ca0-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="a0ca0-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="a0ca0-141">출력</span><span class="sxs-lookup"><span data-stu-id="a0ca0-141">OUTPUTS</span></span>

### <span data-ttu-id="a0ca0-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a0ca0-142">System.Boolean</span></span>

## <span data-ttu-id="a0ca0-143">상속자</span><span class="sxs-lookup"><span data-stu-id="a0ca0-143">NOTES</span></span>

## <span data-ttu-id="a0ca0-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0ca0-144">RELATED LINKS</span></span>
