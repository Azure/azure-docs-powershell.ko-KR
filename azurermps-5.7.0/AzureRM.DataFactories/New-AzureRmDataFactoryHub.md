---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
ms.openlocfilehash: 1891ab463b007b2e4a1502579f0d0e0a48779ca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531734"
---
# <span data-ttu-id="f0e1c-101">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f0e1c-101">New-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="f0e1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e1c-103">Azure Data Factory에 대 한 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-103">Creates a hub for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0e1c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0e1c-104">SYNTAX</span></span>

### <span data-ttu-id="f0e1c-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f0e1c-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0e1c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f0e1c-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0e1c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f0e1c-107">DESCRIPTION</span></span>
<span data-ttu-id="f0e1c-108">**AzureRmDataFactoryHub** cmdlet은 지정 된 azure 리소스 그룹의 Azure Data factory에 대 한 허브를 만들고 지정한 파일 정의를 사용 하 여 지정한 데이터 팩터리에 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-108">The **New-AzureRmDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="f0e1c-109">허브를 만든 후에는 그룹에 연결 된 서비스를 저장 하 고 관리 하는 데 사용할 수 있으며 허브에 파이프라인을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="f0e1c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f0e1c-110">EXAMPLES</span></span>

### <span data-ttu-id="f0e1c-111">예제 1: 허브 만들기</span><span class="sxs-lookup"><span data-stu-id="f0e1c-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="f0e1c-112">이 명령은 리소스 그룹 ADFResourceGroup 및 ADFDataFactory 이라는 data factory에 ContosoDataHub 라는 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="f0e1c-113">변수</span><span class="sxs-lookup"><span data-stu-id="f0e1c-113">PARAMETERS</span></span>

### <span data-ttu-id="f0e1c-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f0e1c-114">-DataFactory</span></span>
<span data-ttu-id="f0e1c-115">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f0e1c-116">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 대 한 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0e1c-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f0e1c-117">-DataFactoryName</span></span>
<span data-ttu-id="f0e1c-118">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f0e1c-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 대 한 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f0e1c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e1c-120">-DefaultProfile</span></span>
<span data-ttu-id="f0e1c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f0e1c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0e1c-122">-파일</span><span class="sxs-lookup"><span data-stu-id="f0e1c-122">-File</span></span>
<span data-ttu-id="f0e1c-123">허브에 대 한 설명을 포함 하는 JSON (JavaScript 개체 표기) 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0e1c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f0e1c-124">-Force</span></span>
<span data-ttu-id="f0e1c-125">이 cmdlet이 사용자에 게 확인을 요청 하지 않고 기존 허브를 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f0e1c-126">-이름</span><span class="sxs-lookup"><span data-stu-id="f0e1c-126">-Name</span></span>
<span data-ttu-id="f0e1c-127">만들 허브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-127">Specifies the name of the hub to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0e1c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0e1c-128">-ResourceGroupName</span></span>
<span data-ttu-id="f0e1c-129">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f0e1c-130">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f0e1c-131">-확인</span><span class="sxs-lookup"><span data-stu-id="f0e1c-131">-Confirm</span></span>
<span data-ttu-id="f0e1c-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0e1c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0e1c-133">-WhatIf</span></span>
<span data-ttu-id="f0e1c-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0e1c-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0e1c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e1c-136">CommonParameters</span></span>
<span data-ttu-id="f0e1c-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e1c-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0e1c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e1c-139">입력</span><span class="sxs-lookup"><span data-stu-id="f0e1c-139">INPUTS</span></span>

### <span data-ttu-id="f0e1c-140">않아야</span><span class="sxs-lookup"><span data-stu-id="f0e1c-140">None</span></span>
<span data-ttu-id="f0e1c-141">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0e1c-142">출력</span><span class="sxs-lookup"><span data-stu-id="f0e1c-142">OUTPUTS</span></span>

### <span data-ttu-id="f0e1c-143">DataFactories. PSHub/.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="f0e1c-144">상속자</span><span class="sxs-lookup"><span data-stu-id="f0e1c-144">NOTES</span></span>
* <span data-ttu-id="f0e1c-145">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="f0e1c-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f0e1c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0e1c-146">RELATED LINKS</span></span>

[<span data-ttu-id="f0e1c-147">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f0e1c-147">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="f0e1c-148">제거-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f0e1c-148">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


