---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: e6dea50e3cb9933d9c6a8aa141f2df43be0b1a18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702734"
---
# <span data-ttu-id="d7932-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="d7932-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="d7932-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7932-102">SYNOPSIS</span></span>
<span data-ttu-id="d7932-103">이 작업은 재해 복구를 사용 하지 않도록 설정 하 고 기본 네임 스페이스로 변경 내용 복제를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7932-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7932-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7932-104">SYNTAX</span></span>

### <span data-ttu-id="d7932-105">GeoDRParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d7932-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7932-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d7932-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7932-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7932-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7932-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d7932-108">DESCRIPTION</span></span>
<span data-ttu-id="d7932-109">**AzureRmEventHubGeoDRConfigurationBreakPair** Cmdlet은 재해 복구를 사용 하지 않도록 설정 하 고 기본 네임 스페이스로 변경 내용 복제를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7932-109">The **Set-AzureRmEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="d7932-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d7932-110">EXAMPLES</span></span>

### <span data-ttu-id="d7932-111">예</span><span class="sxs-lookup"><span data-stu-id="d7932-111">Example</span></span>
```
PS C:\> Set-AzureRmEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="d7932-112">이 작업은 재해 복구를 사용 하지 않도록 설정 하 고 기본 네임 스페이스로 변경 내용 복제를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7932-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="d7932-113">변수</span><span class="sxs-lookup"><span data-stu-id="d7932-113">PARAMETERS</span></span>

### <span data-ttu-id="d7932-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7932-114">-DefaultProfile</span></span>
<span data-ttu-id="d7932-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7932-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7932-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7932-116">-InputObject</span></span>
<span data-ttu-id="d7932-117">Eventhub GeoDR 구성 개체</span><span class="sxs-lookup"><span data-stu-id="d7932-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7932-118">-이름</span><span class="sxs-lookup"><span data-stu-id="d7932-118">-Name</span></span>
<span data-ttu-id="d7932-119">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="d7932-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7932-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d7932-120">-Namespace</span></span>
<span data-ttu-id="d7932-121">네임 스페이스 이름-기본 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="d7932-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7932-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7932-122">-PassThru</span></span>
<span data-ttu-id="d7932-123">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7932-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d7932-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7932-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d7932-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7932-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7932-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d7932-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7932-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7932-127">-ResourceId</span></span>
<span data-ttu-id="d7932-128">GeoDRConfiguration 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="d7932-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7932-129">-확인</span><span class="sxs-lookup"><span data-stu-id="d7932-129">-Confirm</span></span>
<span data-ttu-id="d7932-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7932-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7932-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7932-131">-WhatIf</span></span>
<span data-ttu-id="d7932-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7932-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7932-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7932-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7932-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7932-134">CommonParameters</span></span>
<span data-ttu-id="d7932-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7932-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d7932-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7932-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7932-137">입력</span><span class="sxs-lookup"><span data-stu-id="d7932-137">INPUTS</span></span>

### <span data-ttu-id="d7932-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d7932-138">System.String</span></span>
<span data-ttu-id="d7932-139">PSEventHubDRConfigurationAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="d7932-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="d7932-140">출력</span><span class="sxs-lookup"><span data-stu-id="d7932-140">OUTPUTS</span></span>

### <span data-ttu-id="d7932-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d7932-141">System.Boolean</span></span>


## <span data-ttu-id="d7932-142">상속자</span><span class="sxs-lookup"><span data-stu-id="d7932-142">NOTES</span></span>

## <span data-ttu-id="d7932-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7932-143">RELATED LINKS</span></span>
