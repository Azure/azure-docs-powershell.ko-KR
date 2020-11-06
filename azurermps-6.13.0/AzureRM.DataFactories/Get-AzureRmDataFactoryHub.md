---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: d1015a5f401b0cb91731bafe93ead02e2bf3068f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536679"
---
# <span data-ttu-id="8c3f9-101">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="8c3f9-101">Get-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="8c3f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c3f9-102">SYNOPSIS</span></span>
<span data-ttu-id="8c3f9-103">Azure Data Factory의 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-103">Gets information about hubs in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c3f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8c3f9-104">SYNTAX</span></span>

### <span data-ttu-id="8c3f9-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="8c3f9-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c3f9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8c3f9-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c3f9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8c3f9-107">DESCRIPTION</span></span>
<span data-ttu-id="8c3f9-108">**AzureRmDataFactoryHub** Cmdlet은 Azure Data Factory의 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-108">The **Get-AzureRmDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="8c3f9-109">허브의 이름을 지정 하는 경우이 cmdlet은 해당 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="8c3f9-110">이름을 지정 하지 않으면이 cmdlet은 데이터 팩터리의 모든 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="8c3f9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8c3f9-111">EXAMPLES</span></span>

### <span data-ttu-id="8c3f9-112">예제 1: 모든 데이터 허브 가져오기</span><span class="sxs-lookup"><span data-stu-id="8c3f9-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="8c3f9-113">이 명령은 ADFResourceGroup 이라는 Azure 리소스 그룹의 모든 데이터 허브와 ADFDataFactory 이라는 data factory를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="8c3f9-114">예제 2: 특정 데이터 허브 가져오기</span><span class="sxs-lookup"><span data-stu-id="8c3f9-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="8c3f9-115">이 명령은 ADFResourceGroup 이라는 Azure 리소스 그룹의 MyDataHub 라는 이름과 ADFDataFactory 이라는 data factory에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="8c3f9-116">변수</span><span class="sxs-lookup"><span data-stu-id="8c3f9-116">PARAMETERS</span></span>

### <span data-ttu-id="8c3f9-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c3f9-117">-DataFactory</span></span>
<span data-ttu-id="8c3f9-118">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8c3f9-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8c3f9-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8c3f9-120">-DataFactoryName</span></span>
<span data-ttu-id="8c3f9-121">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8c3f9-122">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8c3f9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c3f9-123">-DefaultProfile</span></span>
<span data-ttu-id="8c3f9-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8c3f9-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c3f9-125">-이름</span><span class="sxs-lookup"><span data-stu-id="8c3f9-125">-Name</span></span>
<span data-ttu-id="8c3f9-126">정보를 가져올 허브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="8c3f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c3f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="8c3f9-128">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8c3f9-129">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8c3f9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c3f9-130">CommonParameters</span></span>
<span data-ttu-id="8c3f9-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c3f9-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c3f9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c3f9-133">입력</span><span class="sxs-lookup"><span data-stu-id="8c3f9-133">INPUTS</span></span>

### <span data-ttu-id="8c3f9-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8c3f9-134">System.String</span></span>

### <span data-ttu-id="8c3f9-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8c3f9-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="8c3f9-136">출력</span><span class="sxs-lookup"><span data-stu-id="8c3f9-136">OUTPUTS</span></span>

### <span data-ttu-id="8c3f9-137">DataFactories. PSHub/.</span><span class="sxs-lookup"><span data-stu-id="8c3f9-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="8c3f9-138">상속자</span><span class="sxs-lookup"><span data-stu-id="8c3f9-138">NOTES</span></span>
* <span data-ttu-id="8c3f9-139">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="8c3f9-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8c3f9-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c3f9-140">RELATED LINKS</span></span>

[<span data-ttu-id="8c3f9-141">새로운 AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="8c3f9-141">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)

[<span data-ttu-id="8c3f9-142">제거-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="8c3f9-142">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


