---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: 6831395c4f3d63dc056729b22573a16d863013e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495628"
---
# <span data-ttu-id="9bac4-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9bac4-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="9bac4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bac4-102">SYNOPSIS</span></span>
<span data-ttu-id="9bac4-103">Azure Data Factory에서 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9bac4-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="9bac4-104">구문</span><span class="sxs-lookup"><span data-stu-id="9bac4-104">SYNTAX</span></span>

### <span data-ttu-id="9bac4-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="9bac4-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bac4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9bac4-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bac4-107">설명</span><span class="sxs-lookup"><span data-stu-id="9bac4-107">DESCRIPTION</span></span>
<span data-ttu-id="9bac4-108">**Remove-AzDataFactoryGateway** cmdlet은 Azure Data Factory에서 지정된 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9bac4-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="9bac4-109">예제</span><span class="sxs-lookup"><span data-stu-id="9bac4-109">EXAMPLES</span></span>

### <span data-ttu-id="9bac4-110">예제 1: 게이트웨이 제거</span><span class="sxs-lookup"><span data-stu-id="9bac4-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="9bac4-111">이 명령은 WikiADF라는 데이터 팩터리에서 ContosoGateway라는 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9bac4-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="9bac4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bac4-112">PARAMETERS</span></span>

### <span data-ttu-id="9bac4-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9bac4-113">-DataFactory</span></span>
<span data-ttu-id="9bac4-114">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="9bac4-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9bac4-115">이 cmdlet은 이 매개 변수가 지정하는 게이트웨이를 데이터 팩터리에서 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9bac4-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9bac4-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9bac4-116">-DataFactoryName</span></span>
<span data-ttu-id="9bac4-117">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9bac4-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9bac4-118">이 cmdlet은 이 매개 변수가 지정하는 게이트웨이를 데이터 팩터리에서 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9bac4-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9bac4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bac4-119">-DefaultProfile</span></span>
<span data-ttu-id="9bac4-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9bac4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bac4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9bac4-121">-Force</span></span>
<span data-ttu-id="9bac4-122">이 cmdlet이 확인을 요청하지 않고 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9bac4-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9bac4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9bac4-123">-Name</span></span>
<span data-ttu-id="9bac4-124">제거할 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9bac4-124">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="9bac4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bac4-125">-ResourceGroupName</span></span>
<span data-ttu-id="9bac4-126">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9bac4-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9bac4-127">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9bac4-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9bac4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bac4-128">-Confirm</span></span>
<span data-ttu-id="9bac4-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bac4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bac4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bac4-130">-WhatIf</span></span>
<span data-ttu-id="9bac4-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9bac4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bac4-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9bac4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bac4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bac4-133">CommonParameters</span></span>
<span data-ttu-id="9bac4-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9bac4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bac4-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9bac4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bac4-136">입력</span><span class="sxs-lookup"><span data-stu-id="9bac4-136">INPUTS</span></span>

### <span data-ttu-id="9bac4-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9bac4-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9bac4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9bac4-138">System.String</span></span>

## <span data-ttu-id="9bac4-139">출력</span><span class="sxs-lookup"><span data-stu-id="9bac4-139">OUTPUTS</span></span>

### <span data-ttu-id="9bac4-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9bac4-140">System.Boolean</span></span>

## <span data-ttu-id="9bac4-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9bac4-141">NOTES</span></span>
* <span data-ttu-id="9bac4-142">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="9bac4-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9bac4-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9bac4-143">RELATED LINKS</span></span>

[<span data-ttu-id="9bac4-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9bac4-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="9bac4-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9bac4-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="9bac4-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9bac4-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


