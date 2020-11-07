---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 73cc7df9dcb32dac592df56f16ad819219e06b7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704070"
---
# <span data-ttu-id="e8f3d-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e8f3d-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="e8f3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f3d-103">Data factory를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f3d-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8f3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e8f3d-104">SYNTAX</span></span>

### <span data-ttu-id="e8f3d-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e8f3d-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e8f3d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e8f3d-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e8f3d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f3d-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e8f3d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e8f3d-108">DESCRIPTION</span></span>
<span data-ttu-id="e8f3d-109">Remove-AzureRmDataFactoryV2 cmdlet은 data factory를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f3d-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="e8f3d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e8f3d-110">EXAMPLES</span></span>

### <span data-ttu-id="e8f3d-111">예제 1: data factory 제거</span><span class="sxs-lookup"><span data-stu-id="e8f3d-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="e8f3d-112">이 명령은 ADF 라는 리소스 그룹에서 WikiADF 이라는 data factory를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f3d-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="e8f3d-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f3d-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="e8f3d-114">변수</span><span class="sxs-lookup"><span data-stu-id="e8f3d-114">PARAMETERS</span></span>

### <span data-ttu-id="e8f3d-115">-확인</span><span class="sxs-lookup"><span data-stu-id="e8f3d-115">-Confirm</span></span>
<span data-ttu-id="e8f3d-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f3d-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f3d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8f3d-117">-InputObject</span></span>
<span data-ttu-id="e8f3d-118">제거할 DataFactory 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f3d-118">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f3d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e8f3d-119">-Force</span></span>
<span data-ttu-id="e8f3d-120">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f3d-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f3d-121">-이름</span><span class="sxs-lookup"><span data-stu-id="e8f3d-121">-Name</span></span>
<span data-ttu-id="e8f3d-122">제거할 데이터 팩터리의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f3d-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f3d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8f3d-123">-ResourceGroupName</span></span>
<span data-ttu-id="e8f3d-124">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f3d-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e8f3d-125">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 데이터 팩터리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8f3d-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f3d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f3d-126">-ResourceId</span></span>
<span data-ttu-id="e8f3d-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e8f3d-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f3d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f3d-128">-WhatIf</span></span>
<span data-ttu-id="e8f3d-129">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e8f3d-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="e8f3d-130">입력</span><span class="sxs-lookup"><span data-stu-id="e8f3d-130">INPUTS</span></span>

### <span data-ttu-id="e8f3d-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e8f3d-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="e8f3d-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e8f3d-132">System.String</span></span>


## <span data-ttu-id="e8f3d-133">출력</span><span class="sxs-lookup"><span data-stu-id="e8f3d-133">OUTPUTS</span></span>

### <span data-ttu-id="e8f3d-134">System. 개체</span><span class="sxs-lookup"><span data-stu-id="e8f3d-134">System.Object</span></span>

## <span data-ttu-id="e8f3d-135">상속자</span><span class="sxs-lookup"><span data-stu-id="e8f3d-135">NOTES</span></span>
<span data-ttu-id="e8f3d-136">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="e8f3d-136">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e8f3d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8f3d-137">RELATED LINKS</span></span>
[<span data-ttu-id="e8f3d-138">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e8f3d-138">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="e8f3d-139">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e8f3d-139">Set-AzureRmDataFactoryV2</span></span>]()
