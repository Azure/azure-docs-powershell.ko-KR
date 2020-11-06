---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: 02949f3a16c9a259e645a035ce3e762db9582024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528853"
---
# <span data-ttu-id="ba8d8-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="ba8d8-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="ba8d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8d8-103">지정 된 릴레이 네임 스페이스에서 WcfRelay를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba8d8-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba8d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba8d8-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba8d8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ba8d8-105">DESCRIPTION</span></span>
<span data-ttu-id="ba8d8-106">**Remove-AzureRmWcfRelay** cmdlet은 지정 된 릴레이 네임 스페이스에서 WcfRelay를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba8d8-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="ba8d8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ba8d8-107">EXAMPLES</span></span>

### <span data-ttu-id="ba8d8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba8d8-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="ba8d8-109">네임 스페이스에서 WcfRelay를 제거 합니다 `TestWCFRelay1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ba8d8-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="ba8d8-110">변수</span><span class="sxs-lookup"><span data-stu-id="ba8d8-110">PARAMETERS</span></span>

### <span data-ttu-id="ba8d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8d8-111">-DefaultProfile</span></span>
<span data-ttu-id="ba8d8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba8d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba8d8-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ba8d8-113">-Name</span></span>
<span data-ttu-id="ba8d8-114">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba8d8-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="ba8d8-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ba8d8-115">-Namespace</span></span>
<span data-ttu-id="ba8d8-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba8d8-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8d8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba8d8-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba8d8-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba8d8-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8d8-119">-확인</span><span class="sxs-lookup"><span data-stu-id="ba8d8-119">-Confirm</span></span>
<span data-ttu-id="ba8d8-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba8d8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba8d8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba8d8-121">-WhatIf</span></span>
<span data-ttu-id="ba8d8-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ba8d8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba8d8-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba8d8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba8d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8d8-124">CommonParameters</span></span>
<span data-ttu-id="ba8d8-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba8d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8d8-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba8d8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8d8-127">입력</span><span class="sxs-lookup"><span data-stu-id="ba8d8-127">INPUTS</span></span>

### <span data-ttu-id="ba8d8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba8d8-128">-ResourceGroupName</span></span>
 <span data-ttu-id="ba8d8-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ba8d8-129">System.String</span></span>
 

### <span data-ttu-id="ba8d8-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ba8d8-130">-Namespace</span></span>
 <span data-ttu-id="ba8d8-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ba8d8-131">System.String</span></span>
 

### <span data-ttu-id="ba8d8-132">-이름</span><span class="sxs-lookup"><span data-stu-id="ba8d8-132">-Name</span></span>
 <span data-ttu-id="ba8d8-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ba8d8-133">System.String</span></span>

## <span data-ttu-id="ba8d8-134">출력</span><span class="sxs-lookup"><span data-stu-id="ba8d8-134">OUTPUTS</span></span>

### <span data-ttu-id="ba8d8-135">System. 개체</span><span class="sxs-lookup"><span data-stu-id="ba8d8-135">System.Object</span></span>

## <span data-ttu-id="ba8d8-136">상속자</span><span class="sxs-lookup"><span data-stu-id="ba8d8-136">NOTES</span></span>

## <span data-ttu-id="ba8d8-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba8d8-137">RELATED LINKS</span></span>

