---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 929ebdfb9cc38d5233027da75752f4c82c484536
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530533"
---
# <span data-ttu-id="6d68c-101">Remove-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d68c-101">Remove-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="6d68c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d68c-102">SYNOPSIS</span></span>
<span data-ttu-id="6d68c-103">별칭을 삭제 합니다 (재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="6d68c-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d68c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d68c-104">SYNTAX</span></span>

### <span data-ttu-id="6d68c-105">GeoDRParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6d68c-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d68c-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6d68c-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d68c-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d68c-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d68c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6d68c-108">DESCRIPTION</span></span>
<span data-ttu-id="6d68c-109">AzureRmEventHubGeoDRConfiguration cmdlet이 별칭 (재해 복구 구성)을 삭제 **함**</span><span class="sxs-lookup"><span data-stu-id="6d68c-109">The **Remove-AzureRmEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="6d68c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6d68c-110">EXAMPLES</span></span>

### <span data-ttu-id="6d68c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d68c-111">Example 1</span></span>
```
PS C:\>Remove-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="6d68c-112">별칭을 삭제 합니다 (재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="6d68c-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="6d68c-113">변수</span><span class="sxs-lookup"><span data-stu-id="6d68c-113">PARAMETERS</span></span>

### <span data-ttu-id="6d68c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d68c-114">-AsJob</span></span>
<span data-ttu-id="6d68c-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6d68c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d68c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d68c-116">-DefaultProfile</span></span>
<span data-ttu-id="6d68c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d68c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d68c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d68c-118">-InputObject</span></span>
<span data-ttu-id="6d68c-119">Eventhub GeoDR 구성 개체</span><span class="sxs-lookup"><span data-stu-id="6d68c-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="6d68c-120">-이름</span><span class="sxs-lookup"><span data-stu-id="6d68c-120">-Name</span></span>
<span data-ttu-id="6d68c-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="6d68c-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="6d68c-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6d68c-122">-Namespace</span></span>
<span data-ttu-id="6d68c-123">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="6d68c-123">Namespace Name</span></span>

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

### <span data-ttu-id="6d68c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d68c-124">-PassThru</span></span>
<span data-ttu-id="6d68c-125">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d68c-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6d68c-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d68c-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6d68c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d68c-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d68c-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6d68c-128">Resource Group Name</span></span>

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

### <span data-ttu-id="6d68c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d68c-129">-ResourceId</span></span>
<span data-ttu-id="6d68c-130">GeoDRConfiguration 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="6d68c-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="6d68c-131">-확인</span><span class="sxs-lookup"><span data-stu-id="6d68c-131">-Confirm</span></span>
<span data-ttu-id="6d68c-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d68c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d68c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d68c-133">-WhatIf</span></span>
<span data-ttu-id="6d68c-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d68c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d68c-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d68c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d68c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d68c-136">CommonParameters</span></span>
<span data-ttu-id="6d68c-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d68c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6d68c-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d68c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d68c-139">입력</span><span class="sxs-lookup"><span data-stu-id="6d68c-139">INPUTS</span></span>

### <span data-ttu-id="6d68c-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6d68c-140">System.String</span></span>
<span data-ttu-id="6d68c-141">PSEventHubDRConfigurationAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="6d68c-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="6d68c-142">출력</span><span class="sxs-lookup"><span data-stu-id="6d68c-142">OUTPUTS</span></span>

### <span data-ttu-id="6d68c-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6d68c-143">System.Boolean</span></span>


## <span data-ttu-id="6d68c-144">상속자</span><span class="sxs-lookup"><span data-stu-id="6d68c-144">NOTES</span></span>

## <span data-ttu-id="6d68c-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d68c-145">RELATED LINKS</span></span>
