---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: c396455804f6bb501fa6439fceffb0eb45875516
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495621"
---
# <span data-ttu-id="7bcf1-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7bcf1-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="7bcf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bcf1-102">SYNOPSIS</span></span>
<span data-ttu-id="7bcf1-103">데이터 팩터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-103">Removes a data factory.</span></span>

## <span data-ttu-id="7bcf1-104">구문</span><span class="sxs-lookup"><span data-stu-id="7bcf1-104">SYNTAX</span></span>

### <span data-ttu-id="7bcf1-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7bcf1-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bcf1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7bcf1-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bcf1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7bcf1-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bcf1-108">설명</span><span class="sxs-lookup"><span data-stu-id="7bcf1-108">DESCRIPTION</span></span>
<span data-ttu-id="7bcf1-109">Remove-AzDataFactoryV2 cmdlet은 데이터 팩터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="7bcf1-110">예제</span><span class="sxs-lookup"><span data-stu-id="7bcf1-110">EXAMPLES</span></span>

### <span data-ttu-id="7bcf1-111">예제 1: 데이터 팩터리 제거</span><span class="sxs-lookup"><span data-stu-id="7bcf1-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="7bcf1-112">이 명령은 ADF라는 리소스 그룹에서 WikiADF라는 데이터 팩터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="7bcf1-113">이 명령은 $True.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="7bcf1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bcf1-114">PARAMETERS</span></span>

### <span data-ttu-id="7bcf1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bcf1-115">-DefaultProfile</span></span>
<span data-ttu-id="7bcf1-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bcf1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7bcf1-117">-Force</span></span>
<span data-ttu-id="7bcf1-118">확인 메시지를 표시하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7bcf1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bcf1-119">-InputObject</span></span>
<span data-ttu-id="7bcf1-120">제거할 DataFactory 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bcf1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7bcf1-121">-Name</span></span>
<span data-ttu-id="7bcf1-122">제거할 데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bcf1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bcf1-123">-ResourceGroupName</span></span>
<span data-ttu-id="7bcf1-124">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7bcf1-125">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 데이터 팩터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bcf1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bcf1-126">-ResourceId</span></span>
<span data-ttu-id="7bcf1-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bcf1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bcf1-128">-Confirm</span></span>
<span data-ttu-id="7bcf1-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bcf1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bcf1-130">-WhatIf</span></span>
<span data-ttu-id="7bcf1-131">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7bcf1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bcf1-132">CommonParameters</span></span>
<span data-ttu-id="7bcf1-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bcf1-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bcf1-135">입력</span><span class="sxs-lookup"><span data-stu-id="7bcf1-135">INPUTS</span></span>

### <span data-ttu-id="7bcf1-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7bcf1-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="7bcf1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="7bcf1-137">System.String</span></span>

## <span data-ttu-id="7bcf1-138">출력</span><span class="sxs-lookup"><span data-stu-id="7bcf1-138">OUTPUTS</span></span>

### <span data-ttu-id="7bcf1-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="7bcf1-139">System.Void</span></span>

## <span data-ttu-id="7bcf1-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7bcf1-140">NOTES</span></span>
<span data-ttu-id="7bcf1-141">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="7bcf1-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7bcf1-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7bcf1-142">RELATED LINKS</span></span>

[<span data-ttu-id="7bcf1-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7bcf1-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="7bcf1-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7bcf1-144">Set-AzDataFactoryV2</span></span>]()
