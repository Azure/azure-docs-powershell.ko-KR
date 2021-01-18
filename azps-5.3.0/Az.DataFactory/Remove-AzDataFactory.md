---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 36c22a432d4e281600a1b718c1ac58a851fb7069
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495630"
---
# <span data-ttu-id="6ad7f-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="6ad7f-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="6ad7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ad7f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad7f-103">데이터 팩터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad7f-103">Removes a data factory.</span></span>

## <span data-ttu-id="6ad7f-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ad7f-104">SYNTAX</span></span>

### <span data-ttu-id="6ad7f-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="6ad7f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad7f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6ad7f-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ad7f-107">설명</span><span class="sxs-lookup"><span data-stu-id="6ad7f-107">DESCRIPTION</span></span>
<span data-ttu-id="6ad7f-108">**Remove-AzDataFactory** cmdlet은 데이터 팩터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad7f-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="6ad7f-109">예제</span><span class="sxs-lookup"><span data-stu-id="6ad7f-109">EXAMPLES</span></span>

### <span data-ttu-id="6ad7f-110">예제 1: 데이터 팩터리 제거</span><span class="sxs-lookup"><span data-stu-id="6ad7f-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="6ad7f-111">이 명령은 ADF라는 리소스 그룹에서 WikiADF라는 데이터 팩터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad7f-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="6ad7f-112">이 명령은 $True.</span><span class="sxs-lookup"><span data-stu-id="6ad7f-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="6ad7f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ad7f-113">PARAMETERS</span></span>

### <span data-ttu-id="6ad7f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ad7f-114">-DataFactory</span></span>
<span data-ttu-id="6ad7f-115">제거할 **PSDataFactory 개체를** 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad7f-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="6ad7f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad7f-116">-DefaultProfile</span></span>
<span data-ttu-id="6ad7f-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6ad7f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ad7f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6ad7f-118">-Force</span></span>
<span data-ttu-id="6ad7f-119">이 cmdlet이 확인을 요청하지 않고 데이터 팩터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad7f-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="6ad7f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6ad7f-120">-Name</span></span>
<span data-ttu-id="6ad7f-121">제거할 데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad7f-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad7f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad7f-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ad7f-123">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad7f-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6ad7f-124">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 데이터 팩터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad7f-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6ad7f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ad7f-125">-Confirm</span></span>
<span data-ttu-id="6ad7f-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ad7f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad7f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad7f-127">-WhatIf</span></span>
<span data-ttu-id="6ad7f-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6ad7f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ad7f-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ad7f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ad7f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad7f-130">CommonParameters</span></span>
<span data-ttu-id="6ad7f-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad7f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad7f-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6ad7f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad7f-133">입력</span><span class="sxs-lookup"><span data-stu-id="6ad7f-133">INPUTS</span></span>

### <span data-ttu-id="6ad7f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6ad7f-134">System.String</span></span>

### <span data-ttu-id="6ad7f-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6ad7f-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="6ad7f-136">출력</span><span class="sxs-lookup"><span data-stu-id="6ad7f-136">OUTPUTS</span></span>

### <span data-ttu-id="6ad7f-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="6ad7f-137">System.Void</span></span>

## <span data-ttu-id="6ad7f-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ad7f-138">NOTES</span></span>
* <span data-ttu-id="6ad7f-139">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="6ad7f-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6ad7f-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ad7f-140">RELATED LINKS</span></span>

[<span data-ttu-id="6ad7f-141">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="6ad7f-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="6ad7f-142">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="6ad7f-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)


