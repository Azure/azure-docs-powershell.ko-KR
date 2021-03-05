---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 8144d1989f6bec9c1342613cf4776a6dae0a9c27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972059"
---
# <span data-ttu-id="c1dc0-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="c1dc0-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="c1dc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="c1dc0-103">Azure Data Factory에서 허브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="c1dc0-104">구문</span><span class="sxs-lookup"><span data-stu-id="c1dc0-104">SYNTAX</span></span>

### <span data-ttu-id="c1dc0-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c1dc0-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1dc0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c1dc0-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1dc0-107">설명</span><span class="sxs-lookup"><span data-stu-id="c1dc0-107">DESCRIPTION</span></span>
<span data-ttu-id="c1dc0-108">**Remove-AzDataFactoryHub** cmdlet은 지정된 Azure 리소스 그룹 및 지정된 데이터 팩터리에서 Azure Data Factory에서 허브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="c1dc0-109">허브를 제거하면 허브의 모든 연결된 서비스 및 파이프라인도 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="c1dc0-110">예제</span><span class="sxs-lookup"><span data-stu-id="c1dc0-110">EXAMPLES</span></span>

### <span data-ttu-id="c1dc0-111">예제 1: 허브 제거</span><span class="sxs-lookup"><span data-stu-id="c1dc0-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="c1dc0-112">이 명령은 ADFResourceGroup이라는 Azure 리소스 그룹과 ADFDataFactory라는 데이터 팩터리에서 ContosoDataHub라는 허브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="c1dc0-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c1dc0-113">PARAMETERS</span></span>

### <span data-ttu-id="c1dc0-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1dc0-114">-DataFactory</span></span>
<span data-ttu-id="c1dc0-115">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="c1dc0-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c1dc0-116">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 허브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c1dc0-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c1dc0-117">-DataFactoryName</span></span>
<span data-ttu-id="c1dc0-118">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c1dc0-119">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 허브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c1dc0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1dc0-120">-DefaultProfile</span></span>
<span data-ttu-id="c1dc0-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c1dc0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1dc0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c1dc0-122">-Force</span></span>
<span data-ttu-id="c1dc0-123">확인을 요청하지 않고 허브를 제거한 이 cmdlet을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c1dc0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c1dc0-124">-Name</span></span>
<span data-ttu-id="c1dc0-125">제거할 허브의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-125">Specifies the name of the hub to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1dc0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1dc0-126">-ResourceGroupName</span></span>
<span data-ttu-id="c1dc0-127">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c1dc0-128">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 허브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c1dc0-129">-확인</span><span class="sxs-lookup"><span data-stu-id="c1dc0-129">-Confirm</span></span>
<span data-ttu-id="c1dc0-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1dc0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1dc0-131">-WhatIf</span></span>
<span data-ttu-id="c1dc0-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1dc0-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1dc0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1dc0-134">CommonParameters</span></span>
<span data-ttu-id="c1dc0-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1dc0-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c1dc0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1dc0-137">입력</span><span class="sxs-lookup"><span data-stu-id="c1dc0-137">INPUTS</span></span>

### <span data-ttu-id="c1dc0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c1dc0-138">System.String</span></span>

### <span data-ttu-id="c1dc0-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c1dc0-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="c1dc0-140">출력</span><span class="sxs-lookup"><span data-stu-id="c1dc0-140">OUTPUTS</span></span>

### <span data-ttu-id="c1dc0-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1dc0-141">System.Boolean</span></span>

## <span data-ttu-id="c1dc0-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c1dc0-142">NOTES</span></span>
* <span data-ttu-id="c1dc0-143">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="c1dc0-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c1dc0-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1dc0-144">RELATED LINKS</span></span>

[<span data-ttu-id="c1dc0-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="c1dc0-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="c1dc0-146">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="c1dc0-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


