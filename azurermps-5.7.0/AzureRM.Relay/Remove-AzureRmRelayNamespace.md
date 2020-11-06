---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: 52abd413f94d0c190a6f03b3707efdb544a4b72a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528854"
---
# <span data-ttu-id="accf0-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="accf0-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="accf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="accf0-102">SYNOPSIS</span></span>
<span data-ttu-id="accf0-103">지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="accf0-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="accf0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="accf0-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="accf0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="accf0-105">DESCRIPTION</span></span>
<span data-ttu-id="accf0-106">**AzureRmRelayNamespace** cmdlet은 지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="accf0-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="accf0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="accf0-107">EXAMPLES</span></span>

### <span data-ttu-id="accf0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="accf0-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="accf0-109">지정 된 리소스 그룹에서 릴레이 네임 스페이스를 제거 `TestNameSpace-Relay1` `Default-ServiceBus-WestUS` 합니다.</span><span class="sxs-lookup"><span data-stu-id="accf0-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="accf0-110">변수</span><span class="sxs-lookup"><span data-stu-id="accf0-110">PARAMETERS</span></span>

### <span data-ttu-id="accf0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="accf0-111">-DefaultProfile</span></span>
<span data-ttu-id="accf0-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="accf0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="accf0-113">-이름</span><span class="sxs-lookup"><span data-stu-id="accf0-113">-Name</span></span>
<span data-ttu-id="accf0-114">릴레이 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="accf0-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="accf0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="accf0-115">-ResourceGroupName</span></span>
<span data-ttu-id="accf0-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="accf0-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="accf0-117">-확인</span><span class="sxs-lookup"><span data-stu-id="accf0-117">-Confirm</span></span>
<span data-ttu-id="accf0-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="accf0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="accf0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="accf0-119">-WhatIf</span></span>
<span data-ttu-id="accf0-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="accf0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="accf0-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="accf0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="accf0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="accf0-122">CommonParameters</span></span>
<span data-ttu-id="accf0-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="accf0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="accf0-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="accf0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="accf0-125">입력</span><span class="sxs-lookup"><span data-stu-id="accf0-125">INPUTS</span></span>

### <span data-ttu-id="accf0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="accf0-126">-ResourceGroupName</span></span>
 <span data-ttu-id="accf0-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="accf0-127">System.String</span></span>

### <span data-ttu-id="accf0-128">-이름</span><span class="sxs-lookup"><span data-stu-id="accf0-128">-Name</span></span>
 <span data-ttu-id="accf0-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="accf0-129">System.String</span></span>

## <span data-ttu-id="accf0-130">출력</span><span class="sxs-lookup"><span data-stu-id="accf0-130">OUTPUTS</span></span>

### <span data-ttu-id="accf0-131">System. 개체</span><span class="sxs-lookup"><span data-stu-id="accf0-131">System.Object</span></span>

## <span data-ttu-id="accf0-132">상속자</span><span class="sxs-lookup"><span data-stu-id="accf0-132">NOTES</span></span>

## <span data-ttu-id="accf0-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="accf0-133">RELATED LINKS</span></span>

