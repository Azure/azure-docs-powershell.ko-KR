---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 84608cbe83d54d562877aa2ada4527fbc636996f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697080"
---
# <span data-ttu-id="8900b-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="8900b-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="8900b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8900b-102">SYNOPSIS</span></span>
<span data-ttu-id="8900b-103">Azure Data Factory의 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="8900b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8900b-104">SYNTAX</span></span>

### <span data-ttu-id="8900b-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="8900b-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8900b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8900b-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8900b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8900b-107">DESCRIPTION</span></span>
<span data-ttu-id="8900b-108">**AzDataFactoryHub** Cmdlet은 Azure Data Factory의 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="8900b-109">허브의 이름을 지정 하는 경우이 cmdlet은 해당 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="8900b-110">이름을 지정 하지 않으면이 cmdlet은 데이터 팩터리의 모든 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="8900b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8900b-111">EXAMPLES</span></span>

### <span data-ttu-id="8900b-112">예제 1: 모든 데이터 허브 가져오기</span><span class="sxs-lookup"><span data-stu-id="8900b-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="8900b-113">이 명령은 ADFResourceGroup 이라는 Azure 리소스 그룹의 모든 데이터 허브와 ADFDataFactory 이라는 data factory를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="8900b-114">예제 2: 특정 데이터 허브 가져오기</span><span class="sxs-lookup"><span data-stu-id="8900b-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="8900b-115">이 명령은 ADFResourceGroup 이라는 Azure 리소스 그룹의 MyDataHub 라는 이름과 ADFDataFactory 이라는 data factory에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="8900b-116">변수</span><span class="sxs-lookup"><span data-stu-id="8900b-116">PARAMETERS</span></span>

### <span data-ttu-id="8900b-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8900b-117">-DataFactory</span></span>
<span data-ttu-id="8900b-118">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8900b-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8900b-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8900b-120">-DataFactoryName</span></span>
<span data-ttu-id="8900b-121">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8900b-122">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8900b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8900b-123">-DefaultProfile</span></span>
<span data-ttu-id="8900b-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8900b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8900b-125">-이름</span><span class="sxs-lookup"><span data-stu-id="8900b-125">-Name</span></span>
<span data-ttu-id="8900b-126">정보를 가져올 허브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="8900b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8900b-127">-ResourceGroupName</span></span>
<span data-ttu-id="8900b-128">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8900b-129">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8900b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8900b-130">CommonParameters</span></span>
<span data-ttu-id="8900b-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8900b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8900b-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8900b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8900b-133">입력</span><span class="sxs-lookup"><span data-stu-id="8900b-133">INPUTS</span></span>

### <span data-ttu-id="8900b-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8900b-134">System.String</span></span>

### <span data-ttu-id="8900b-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8900b-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="8900b-136">출력</span><span class="sxs-lookup"><span data-stu-id="8900b-136">OUTPUTS</span></span>

### <span data-ttu-id="8900b-137">DataFactories. PSHub/.</span><span class="sxs-lookup"><span data-stu-id="8900b-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="8900b-138">상속자</span><span class="sxs-lookup"><span data-stu-id="8900b-138">NOTES</span></span>
* <span data-ttu-id="8900b-139">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="8900b-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8900b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8900b-140">RELATED LINKS</span></span>

[<span data-ttu-id="8900b-141">새로운 AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="8900b-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="8900b-142">제거-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="8900b-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


