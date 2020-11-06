---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
ms.openlocfilehash: 4ee22c46a3754bcb8378acb3b37da96bd11090fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530549"
---
# <span data-ttu-id="a59e2-101">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="a59e2-101">Remove-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="a59e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a59e2-102">SYNOPSIS</span></span>
<span data-ttu-id="a59e2-103">Azure Data Factory에서 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-103">Removes a hub from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a59e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a59e2-104">SYNTAX</span></span>

### <span data-ttu-id="a59e2-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a59e2-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a59e2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a59e2-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a59e2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a59e2-107">DESCRIPTION</span></span>
<span data-ttu-id="a59e2-108">**AzureRmDataFactoryHub** cmdlet은 지정 된 azure 리소스 그룹의 Azure Data factory 및 지정 된 Data factory에서 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-108">The **Remove-AzureRmDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="a59e2-109">허브를 제거 하면 허브에 연결 된 모든 서비스 및 파이프라인이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="a59e2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a59e2-110">EXAMPLES</span></span>

### <span data-ttu-id="a59e2-111">예제 1: 허브 제거</span><span class="sxs-lookup"><span data-stu-id="a59e2-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="a59e2-112">이 명령은 ADFResourceGroup 이라는 Azure 리소스 그룹 및 ADFDataFactory 라는 data factory에서 ContosoDataHub 라는 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="a59e2-113">변수</span><span class="sxs-lookup"><span data-stu-id="a59e2-113">PARAMETERS</span></span>

### <span data-ttu-id="a59e2-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a59e2-114">-DataFactory</span></span>
<span data-ttu-id="a59e2-115">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a59e2-116">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a59e2-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a59e2-117">-DataFactoryName</span></span>
<span data-ttu-id="a59e2-118">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a59e2-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a59e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a59e2-120">-DefaultProfile</span></span>
<span data-ttu-id="a59e2-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a59e2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a59e2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a59e2-122">-Force</span></span>
<span data-ttu-id="a59e2-123">이 cmdlet이 확인 메시지를 표시 하지 않고 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a59e2-124">-이름</span><span class="sxs-lookup"><span data-stu-id="a59e2-124">-Name</span></span>
<span data-ttu-id="a59e2-125">제거할 허브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-125">Specifies the name of the hub to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a59e2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a59e2-126">-ResourceGroupName</span></span>
<span data-ttu-id="a59e2-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a59e2-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a59e2-129">-확인</span><span class="sxs-lookup"><span data-stu-id="a59e2-129">-Confirm</span></span>
<span data-ttu-id="a59e2-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a59e2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a59e2-131">-WhatIf</span></span>
<span data-ttu-id="a59e2-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a59e2-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a59e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a59e2-134">CommonParameters</span></span>
<span data-ttu-id="a59e2-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a59e2-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a59e2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a59e2-137">입력</span><span class="sxs-lookup"><span data-stu-id="a59e2-137">INPUTS</span></span>

### <span data-ttu-id="a59e2-138">않아야</span><span class="sxs-lookup"><span data-stu-id="a59e2-138">None</span></span>
<span data-ttu-id="a59e2-139">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a59e2-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a59e2-140">출력</span><span class="sxs-lookup"><span data-stu-id="a59e2-140">OUTPUTS</span></span>

### <span data-ttu-id="a59e2-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a59e2-141">System.Boolean</span></span>

## <span data-ttu-id="a59e2-142">상속자</span><span class="sxs-lookup"><span data-stu-id="a59e2-142">NOTES</span></span>
* <span data-ttu-id="a59e2-143">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="a59e2-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a59e2-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a59e2-144">RELATED LINKS</span></span>

[<span data-ttu-id="a59e2-145">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="a59e2-145">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="a59e2-146">새로운 AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="a59e2-146">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)


