---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198889"
---
# <span data-ttu-id="d348d-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="d348d-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="d348d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d348d-102">SYNOPSIS</span></span>
<span data-ttu-id="d348d-103">Azure Data Factory의 허브에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="d348d-104">구문</span><span class="sxs-lookup"><span data-stu-id="d348d-104">SYNTAX</span></span>

### <span data-ttu-id="d348d-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d348d-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d348d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d348d-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d348d-107">설명</span><span class="sxs-lookup"><span data-stu-id="d348d-107">DESCRIPTION</span></span>
<span data-ttu-id="d348d-108">**Get-AzDataFactoryHub** cmdlet은 Azure Data Factory의 허브에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="d348d-109">허브의 이름을 지정하는 경우 이 cmdlet은 해당 허브에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="d348d-110">이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 허브에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="d348d-111">예제</span><span class="sxs-lookup"><span data-stu-id="d348d-111">EXAMPLES</span></span>

### <span data-ttu-id="d348d-112">예제 1: 모든 데이터 허브를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="d348d-113">이 명령은 ADFResourceGroup이라는 Azure 리소스 그룹 및 ADFDataFactory라는 데이터 팩터리의 모든 데이터 허브를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="d348d-114">예제 2: 특정 데이터 허브를 얻게</span><span class="sxs-lookup"><span data-stu-id="d348d-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="d348d-115">이 명령은 ADFResourceGroup이라는 Azure 리소스 그룹에 MyDataHub라는 허브 및 ADFDataFactory라는 데이터 팩터리에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="d348d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d348d-116">PARAMETERS</span></span>

### <span data-ttu-id="d348d-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d348d-117">-DataFactory</span></span>
<span data-ttu-id="d348d-118">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="d348d-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d348d-119">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리의 허브에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d348d-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d348d-120">-DataFactoryName</span></span>
<span data-ttu-id="d348d-121">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d348d-122">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리의 허브에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d348d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d348d-123">-DefaultProfile</span></span>
<span data-ttu-id="d348d-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d348d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d348d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d348d-125">-Name</span></span>
<span data-ttu-id="d348d-126">정보를 얻을 허브의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-126">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d348d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d348d-127">-ResourceGroupName</span></span>
<span data-ttu-id="d348d-128">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d348d-129">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속한 허브에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d348d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d348d-130">CommonParameters</span></span>
<span data-ttu-id="d348d-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d348d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d348d-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d348d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d348d-133">입력</span><span class="sxs-lookup"><span data-stu-id="d348d-133">INPUTS</span></span>

### <span data-ttu-id="d348d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d348d-134">System.String</span></span>

### <span data-ttu-id="d348d-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d348d-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="d348d-136">출력</span><span class="sxs-lookup"><span data-stu-id="d348d-136">OUTPUTS</span></span>

### <span data-ttu-id="d348d-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="d348d-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="d348d-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d348d-138">NOTES</span></span>
* <span data-ttu-id="d348d-139">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="d348d-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d348d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d348d-140">RELATED LINKS</span></span>

[<span data-ttu-id="d348d-141">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="d348d-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="d348d-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="d348d-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


