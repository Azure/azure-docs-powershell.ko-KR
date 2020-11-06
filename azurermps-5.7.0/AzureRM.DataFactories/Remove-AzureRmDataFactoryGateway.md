---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
ms.openlocfilehash: b781207bae8b967acadf4a9ef3ae50c5ffc9cfef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530547"
---
# <span data-ttu-id="33207-101">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="33207-101">Remove-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="33207-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33207-102">SYNOPSIS</span></span>
<span data-ttu-id="33207-103">Azure Data Factory에서 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33207-103">Removes a gateway from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33207-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33207-104">SYNTAX</span></span>

### <span data-ttu-id="33207-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="33207-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33207-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="33207-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33207-107">설명은</span><span class="sxs-lookup"><span data-stu-id="33207-107">DESCRIPTION</span></span>
<span data-ttu-id="33207-108">**AzureRmDataFactoryGateway** Cmdlet은 Azure Data Factory에서 지정 된 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33207-108">The **Remove-AzureRmDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="33207-109">예제의</span><span class="sxs-lookup"><span data-stu-id="33207-109">EXAMPLES</span></span>

### <span data-ttu-id="33207-110">예제 1: 게이트웨이 제거</span><span class="sxs-lookup"><span data-stu-id="33207-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzureRmDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="33207-111">이 명령은 WikiADF 이라는 data factory에서 ContosoGateway 이라는 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33207-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="33207-112">변수</span><span class="sxs-lookup"><span data-stu-id="33207-112">PARAMETERS</span></span>

### <span data-ttu-id="33207-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="33207-113">-DataFactory</span></span>
<span data-ttu-id="33207-114">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33207-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="33207-115">이 cmdlet은이 매개 변수에서 지정 하는 게이트웨이를 데이터 팩터리에 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33207-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="33207-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="33207-116">-DataFactoryName</span></span>
<span data-ttu-id="33207-117">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33207-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="33207-118">이 cmdlet은이 매개 변수에서 지정 하는 게이트웨이를 데이터 팩터리에 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33207-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="33207-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33207-119">-DefaultProfile</span></span>
<span data-ttu-id="33207-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="33207-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33207-121">-Force</span><span class="sxs-lookup"><span data-stu-id="33207-121">-Force</span></span>
<span data-ttu-id="33207-122">이 cmdlet이 확인을 묻지 않고 게이트웨이를 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="33207-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="33207-123">-이름</span><span class="sxs-lookup"><span data-stu-id="33207-123">-Name</span></span>
<span data-ttu-id="33207-124">제거할 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33207-124">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="33207-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33207-125">-ResourceGroupName</span></span>
<span data-ttu-id="33207-126">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33207-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="33207-127">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33207-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="33207-128">-확인</span><span class="sxs-lookup"><span data-stu-id="33207-128">-Confirm</span></span>
<span data-ttu-id="33207-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33207-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33207-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33207-130">-WhatIf</span></span>
<span data-ttu-id="33207-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33207-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33207-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33207-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33207-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33207-133">CommonParameters</span></span>
<span data-ttu-id="33207-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33207-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33207-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33207-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33207-136">입력</span><span class="sxs-lookup"><span data-stu-id="33207-136">INPUTS</span></span>

### <span data-ttu-id="33207-137">않아야</span><span class="sxs-lookup"><span data-stu-id="33207-137">None</span></span>
<span data-ttu-id="33207-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33207-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33207-139">출력</span><span class="sxs-lookup"><span data-stu-id="33207-139">OUTPUTS</span></span>

### <span data-ttu-id="33207-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="33207-140">System.Boolean</span></span>

## <span data-ttu-id="33207-141">상속자</span><span class="sxs-lookup"><span data-stu-id="33207-141">NOTES</span></span>
* <span data-ttu-id="33207-142">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="33207-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="33207-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33207-143">RELATED LINKS</span></span>

[<span data-ttu-id="33207-144">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="33207-144">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="33207-145">새로운 AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="33207-145">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="33207-146">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="33207-146">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


