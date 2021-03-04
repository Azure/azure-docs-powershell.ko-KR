---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: eb9100bf4843d7213d2fbb89ac1827ba7ee1e509
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957392"
---
# <span data-ttu-id="c6c3d-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="c6c3d-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="c6c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c3d-103">Azure Data Factory에서 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="c6c3d-104">구문</span><span class="sxs-lookup"><span data-stu-id="c6c3d-104">SYNTAX</span></span>

### <span data-ttu-id="c6c3d-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c6c3d-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6c3d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c6c3d-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6c3d-107">설명</span><span class="sxs-lookup"><span data-stu-id="c6c3d-107">DESCRIPTION</span></span>
<span data-ttu-id="c6c3d-108">**Remove-AzDataFactoryGateway** cmdlet은 Azure Data Factory에서 지정된 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="c6c3d-109">예제</span><span class="sxs-lookup"><span data-stu-id="c6c3d-109">EXAMPLES</span></span>

### <span data-ttu-id="c6c3d-110">예제 1: 게이트웨이 제거</span><span class="sxs-lookup"><span data-stu-id="c6c3d-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="c6c3d-111">이 명령은 WikiADF라는 데이터 팩터리에서 ContosoGateway라는 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="c6c3d-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c6c3d-112">PARAMETERS</span></span>

### <span data-ttu-id="c6c3d-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c6c3d-113">-DataFactory</span></span>
<span data-ttu-id="c6c3d-114">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="c6c3d-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c6c3d-115">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6c3d-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c6c3d-116">-DataFactoryName</span></span>
<span data-ttu-id="c6c3d-117">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c6c3d-118">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6c3d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c3d-119">-DefaultProfile</span></span>
<span data-ttu-id="c6c3d-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c6c3d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6c3d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c6c3d-121">-Force</span></span>
<span data-ttu-id="c6c3d-122">이 cmdlet은 확인을 요청하지 않고 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c6c3d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c6c3d-123">-Name</span></span>
<span data-ttu-id="c6c3d-124">제거할 게이트웨이 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-124">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6c3d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6c3d-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6c3d-126">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c6c3d-127">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6c3d-128">-확인</span><span class="sxs-lookup"><span data-stu-id="c6c3d-128">-Confirm</span></span>
<span data-ttu-id="c6c3d-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c3d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6c3d-130">-WhatIf</span></span>
<span data-ttu-id="c6c3d-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6c3d-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c3d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c3d-133">CommonParameters</span></span>
<span data-ttu-id="c6c3d-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c3d-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c3d-136">입력</span><span class="sxs-lookup"><span data-stu-id="c6c3d-136">INPUTS</span></span>

### <span data-ttu-id="c6c3d-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c6c3d-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="c6c3d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c6c3d-138">System.String</span></span>

## <span data-ttu-id="c6c3d-139">출력</span><span class="sxs-lookup"><span data-stu-id="c6c3d-139">OUTPUTS</span></span>

### <span data-ttu-id="c6c3d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c6c3d-140">System.Boolean</span></span>

## <span data-ttu-id="c6c3d-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c6c3d-141">NOTES</span></span>
* <span data-ttu-id="c6c3d-142">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="c6c3d-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c6c3d-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6c3d-143">RELATED LINKS</span></span>

[<span data-ttu-id="c6c3d-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="c6c3d-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="c6c3d-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="c6c3d-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="c6c3d-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="c6c3d-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


