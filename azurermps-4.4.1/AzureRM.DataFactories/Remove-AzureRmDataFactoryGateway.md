---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
ms.openlocfilehash: d9ae03325afbfe81c47847cb27df75973221667b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531154"
---
# <span data-ttu-id="24527-101">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="24527-101">Remove-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="24527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24527-102">SYNOPSIS</span></span>
<span data-ttu-id="24527-103">Azure Data Factory에서 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24527-103">Removes a gateway from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24527-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24527-104">SYNTAX</span></span>

### <span data-ttu-id="24527-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="24527-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24527-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="24527-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24527-107">설명은</span><span class="sxs-lookup"><span data-stu-id="24527-107">DESCRIPTION</span></span>
<span data-ttu-id="24527-108">**AzureRmDataFactoryGateway** Cmdlet은 Azure Data Factory에서 지정 된 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24527-108">The **Remove-AzureRmDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="24527-109">예제의</span><span class="sxs-lookup"><span data-stu-id="24527-109">EXAMPLES</span></span>

### <span data-ttu-id="24527-110">예제 1: 게이트웨이 제거</span><span class="sxs-lookup"><span data-stu-id="24527-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzureRmDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="24527-111">이 명령은 WikiADF 이라는 data factory에서 ContosoGateway 이라는 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24527-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="24527-112">변수</span><span class="sxs-lookup"><span data-stu-id="24527-112">PARAMETERS</span></span>

### <span data-ttu-id="24527-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="24527-113">-DataFactory</span></span>
<span data-ttu-id="24527-114">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24527-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="24527-115">이 cmdlet은이 매개 변수에서 지정 하는 게이트웨이를 데이터 팩터리에 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24527-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="24527-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="24527-116">-DataFactoryName</span></span>
<span data-ttu-id="24527-117">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24527-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="24527-118">이 cmdlet은이 매개 변수에서 지정 하는 게이트웨이를 데이터 팩터리에 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24527-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="24527-119">-Force</span><span class="sxs-lookup"><span data-stu-id="24527-119">-Force</span></span>
<span data-ttu-id="24527-120">이 cmdlet이 확인을 묻지 않고 게이트웨이를 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="24527-120">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="24527-121">-이름</span><span class="sxs-lookup"><span data-stu-id="24527-121">-Name</span></span>
<span data-ttu-id="24527-122">제거할 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24527-122">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="24527-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24527-123">-ResourceGroupName</span></span>
<span data-ttu-id="24527-124">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24527-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="24527-125">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24527-125">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="24527-126">-확인</span><span class="sxs-lookup"><span data-stu-id="24527-126">-Confirm</span></span>
<span data-ttu-id="24527-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24527-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24527-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24527-128">-WhatIf</span></span>
<span data-ttu-id="24527-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24527-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24527-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24527-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24527-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24527-131">-DefaultProfile</span></span>
<span data-ttu-id="24527-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24527-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24527-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24527-133">CommonParameters</span></span>
<span data-ttu-id="24527-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24527-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24527-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24527-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24527-136">입력</span><span class="sxs-lookup"><span data-stu-id="24527-136">INPUTS</span></span>

## <span data-ttu-id="24527-137">출력</span><span class="sxs-lookup"><span data-stu-id="24527-137">OUTPUTS</span></span>

### <span data-ttu-id="24527-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="24527-138">System.Boolean</span></span>

## <span data-ttu-id="24527-139">상속자</span><span class="sxs-lookup"><span data-stu-id="24527-139">NOTES</span></span>
* <span data-ttu-id="24527-140">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="24527-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="24527-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24527-141">RELATED LINKS</span></span>

[<span data-ttu-id="24527-142">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="24527-142">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="24527-143">새로운 AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="24527-143">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="24527-144">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="24527-144">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


