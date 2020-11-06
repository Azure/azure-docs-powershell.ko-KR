---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 24c84657dd33c5ea313f1d6d2c0710b6a3801afd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538220"
---
# <span data-ttu-id="f117f-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f117f-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="f117f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f117f-102">SYNOPSIS</span></span>
<span data-ttu-id="f117f-103">Data Factory에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f117f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f117f-104">SYNTAX</span></span>

### <span data-ttu-id="f117f-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f117f-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f117f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f117f-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f117f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f117f-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f117f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f117f-108">DESCRIPTION</span></span>
<span data-ttu-id="f117f-109">Remove-AzureRmDataFactoryV2LinkedService cmdlet은 Azure Data Factory에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="f117f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f117f-110">EXAMPLES</span></span>

### <span data-ttu-id="f117f-111">예제 1: 연결 된 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="f117f-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="f117f-112">이 명령은 WikiADF 이라는 data factory에서 LinkedServiceTest 라는 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="f117f-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="f117f-114">변수</span><span class="sxs-lookup"><span data-stu-id="f117f-114">PARAMETERS</span></span>

### <span data-ttu-id="f117f-115">-확인</span><span class="sxs-lookup"><span data-stu-id="f117f-115">-Confirm</span></span>
<span data-ttu-id="f117f-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f117f-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f117f-117">-DataFactoryName</span></span>
<span data-ttu-id="f117f-118">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f117f-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f117f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f117f-120">-Force</span></span>
<span data-ttu-id="f117f-121">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f117f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f117f-122">-InputObject</span></span>
<span data-ttu-id="f117f-123">제거할 LinkedService 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f117f-124">-이름</span><span class="sxs-lookup"><span data-stu-id="f117f-124">-Name</span></span>
<span data-ttu-id="f117f-125">제거할 연결 된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="f117f-126">연결 된 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-126">Name of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f117f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f117f-127">-ResourceGroupName</span></span>
<span data-ttu-id="f117f-128">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f117f-129">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f117f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f117f-130">-ResourceId</span></span>
<span data-ttu-id="f117f-131">제거할 연결 된 서비스의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="f117f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f117f-132">-WhatIf</span></span>
<span data-ttu-id="f117f-133">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f117f-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="f117f-134">입력</span><span class="sxs-lookup"><span data-stu-id="f117f-134">INPUTS</span></span>

### <span data-ttu-id="f117f-135">DataFactoryV2. PSLinkedService/.</span><span class="sxs-lookup"><span data-stu-id="f117f-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="f117f-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f117f-136">System.String</span></span>


## <span data-ttu-id="f117f-137">출력</span><span class="sxs-lookup"><span data-stu-id="f117f-137">OUTPUTS</span></span>

### <span data-ttu-id="f117f-138">System. 개체</span><span class="sxs-lookup"><span data-stu-id="f117f-138">System.Object</span></span>

## <span data-ttu-id="f117f-139">상속자</span><span class="sxs-lookup"><span data-stu-id="f117f-139">NOTES</span></span>
<span data-ttu-id="f117f-140">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="f117f-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f117f-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f117f-141">RELATED LINKS</span></span>
[<span data-ttu-id="f117f-142">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f117f-142">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="f117f-143">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f117f-143">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

