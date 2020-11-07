---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 0136927eea72911e706c3e0062dbc444cf1f9b25
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697006"
---
# <span data-ttu-id="969a3-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="969a3-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="969a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="969a3-102">SYNOPSIS</span></span>
<span data-ttu-id="969a3-103">Azure Data Factory에서 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="969a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="969a3-104">SYNTAX</span></span>

### <span data-ttu-id="969a3-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="969a3-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="969a3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="969a3-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="969a3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="969a3-107">DESCRIPTION</span></span>
<span data-ttu-id="969a3-108">**AzDataFactoryHub** cmdlet은 지정 된 azure 리소스 그룹의 Azure Data factory 및 지정 된 Data factory에서 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="969a3-109">허브를 제거 하면 허브에 연결 된 모든 서비스 및 파이프라인이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="969a3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="969a3-110">EXAMPLES</span></span>

### <span data-ttu-id="969a3-111">예제 1: 허브 제거</span><span class="sxs-lookup"><span data-stu-id="969a3-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="969a3-112">이 명령은 ADFResourceGroup 이라는 Azure 리소스 그룹 및 ADFDataFactory 라는 data factory에서 ContosoDataHub 라는 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="969a3-113">변수</span><span class="sxs-lookup"><span data-stu-id="969a3-113">PARAMETERS</span></span>

### <span data-ttu-id="969a3-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="969a3-114">-DataFactory</span></span>
<span data-ttu-id="969a3-115">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="969a3-116">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="969a3-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="969a3-117">-DataFactoryName</span></span>
<span data-ttu-id="969a3-118">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="969a3-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="969a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969a3-120">-DefaultProfile</span></span>
<span data-ttu-id="969a3-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="969a3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="969a3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="969a3-122">-Force</span></span>
<span data-ttu-id="969a3-123">이 cmdlet이 확인 메시지를 표시 하지 않고 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="969a3-124">-이름</span><span class="sxs-lookup"><span data-stu-id="969a3-124">-Name</span></span>
<span data-ttu-id="969a3-125">제거할 허브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-125">Specifies the name of the hub to remove.</span></span>

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

### <span data-ttu-id="969a3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="969a3-126">-ResourceGroupName</span></span>
<span data-ttu-id="969a3-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="969a3-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="969a3-129">-확인</span><span class="sxs-lookup"><span data-stu-id="969a3-129">-Confirm</span></span>
<span data-ttu-id="969a3-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="969a3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="969a3-131">-WhatIf</span></span>
<span data-ttu-id="969a3-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="969a3-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="969a3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969a3-134">CommonParameters</span></span>
<span data-ttu-id="969a3-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="969a3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969a3-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="969a3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969a3-137">입력</span><span class="sxs-lookup"><span data-stu-id="969a3-137">INPUTS</span></span>

### <span data-ttu-id="969a3-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="969a3-138">System.String</span></span>

### <span data-ttu-id="969a3-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="969a3-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="969a3-140">출력</span><span class="sxs-lookup"><span data-stu-id="969a3-140">OUTPUTS</span></span>

### <span data-ttu-id="969a3-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="969a3-141">System.Boolean</span></span>

## <span data-ttu-id="969a3-142">상속자</span><span class="sxs-lookup"><span data-stu-id="969a3-142">NOTES</span></span>
* <span data-ttu-id="969a3-143">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="969a3-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="969a3-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="969a3-144">RELATED LINKS</span></span>

[<span data-ttu-id="969a3-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="969a3-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="969a3-146">새로운 AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="969a3-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


