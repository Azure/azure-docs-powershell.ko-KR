---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 87a50c69449437401ff26b76b87cf0f334ab8d71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975888"
---
# <span data-ttu-id="8fc47-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="8fc47-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="8fc47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fc47-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc47-103">Data Factory에서 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="8fc47-104">구문</span><span class="sxs-lookup"><span data-stu-id="8fc47-104">SYNTAX</span></span>

### <span data-ttu-id="8fc47-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="8fc47-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fc47-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8fc47-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fc47-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8fc47-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fc47-108">설명</span><span class="sxs-lookup"><span data-stu-id="8fc47-108">DESCRIPTION</span></span>
<span data-ttu-id="8fc47-109">Remove-AzDataFactoryV2LinkedService cmdlet은 Azure Data Factory에서 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="8fc47-110">예제</span><span class="sxs-lookup"><span data-stu-id="8fc47-110">EXAMPLES</span></span>

### <span data-ttu-id="8fc47-111">예제 1: 연결된 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="8fc47-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="8fc47-112">이 명령은 WikiADF라는 데이터 팩터리에서 LinkedServiceTest라는 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="8fc47-113">이 명령은 $True.</span><span class="sxs-lookup"><span data-stu-id="8fc47-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="8fc47-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8fc47-114">PARAMETERS</span></span>

### <span data-ttu-id="8fc47-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8fc47-115">-DataFactoryName</span></span>
<span data-ttu-id="8fc47-116">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8fc47-117">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc47-118">-DefaultProfile</span></span>
<span data-ttu-id="8fc47-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fc47-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8fc47-120">-Force</span></span>
<span data-ttu-id="8fc47-121">확인을 요청하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8fc47-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fc47-122">-InputObject</span></span>
<span data-ttu-id="8fc47-123">제거할 LinkedService 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc47-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8fc47-124">-Name</span></span>
<span data-ttu-id="8fc47-125">제거할 연결된 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="8fc47-126">연결된 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc47-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc47-127">-ResourceGroupName</span></span>
<span data-ttu-id="8fc47-128">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8fc47-129">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc47-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fc47-130">-ResourceId</span></span>
<span data-ttu-id="8fc47-131">제거할 연결된 서비스의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="8fc47-132">-확인</span><span class="sxs-lookup"><span data-stu-id="8fc47-132">-Confirm</span></span>
<span data-ttu-id="8fc47-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fc47-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fc47-134">-WhatIf</span></span>
<span data-ttu-id="8fc47-135">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8fc47-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc47-136">CommonParameters</span></span>
<span data-ttu-id="8fc47-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8fc47-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc47-138">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8fc47-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc47-139">입력</span><span class="sxs-lookup"><span data-stu-id="8fc47-139">INPUTS</span></span>

### <span data-ttu-id="8fc47-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="8fc47-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="8fc47-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8fc47-141">System.String</span></span>

## <span data-ttu-id="8fc47-142">출력</span><span class="sxs-lookup"><span data-stu-id="8fc47-142">OUTPUTS</span></span>

### <span data-ttu-id="8fc47-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="8fc47-143">System.Void</span></span>

## <span data-ttu-id="8fc47-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8fc47-144">NOTES</span></span>
<span data-ttu-id="8fc47-145">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="8fc47-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8fc47-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8fc47-146">RELATED LINKS</span></span>

[<span data-ttu-id="8fc47-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="8fc47-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="8fc47-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="8fc47-148">Set-AzDataFactoryV2LinkedService</span></span>]()

