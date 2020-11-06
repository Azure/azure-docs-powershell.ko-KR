---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 746033cfdf48782d10c0fdabf7a018d309269afb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524287"
---
# <span data-ttu-id="bb79c-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="bb79c-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="bb79c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb79c-102">SYNOPSIS</span></span>
<span data-ttu-id="bb79c-103">지정 된 HybridConnection 네임 스페이스에서 HybridConnection를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb79c-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb79c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb79c-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb79c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bb79c-105">DESCRIPTION</span></span>
<span data-ttu-id="bb79c-106">**Remove-AzureRmRelayHybridConnection** cmdlet은 지정 된 릴레이 네임 스페이스에서 HybridConnection를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb79c-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="bb79c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bb79c-107">EXAMPLES</span></span>

### <span data-ttu-id="bb79c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb79c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="bb79c-109">네임 스페이스에서 HybridConnection를 제거 합니다 `TestHybridConnection` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="bb79c-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="bb79c-110">변수</span><span class="sxs-lookup"><span data-stu-id="bb79c-110">PARAMETERS</span></span>

### <span data-ttu-id="bb79c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb79c-111">-DefaultProfile</span></span>
<span data-ttu-id="bb79c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb79c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb79c-113">-이름</span><span class="sxs-lookup"><span data-stu-id="bb79c-113">-Name</span></span>
<span data-ttu-id="bb79c-114">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb79c-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="bb79c-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bb79c-115">-Namespace</span></span>
<span data-ttu-id="bb79c-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb79c-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb79c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb79c-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb79c-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb79c-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb79c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="bb79c-119">-Confirm</span></span>
<span data-ttu-id="bb79c-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb79c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb79c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb79c-121">-WhatIf</span></span>
<span data-ttu-id="bb79c-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bb79c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb79c-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb79c-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb79c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb79c-124">CommonParameters</span></span>
<span data-ttu-id="bb79c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb79c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bb79c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb79c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb79c-127">입력</span><span class="sxs-lookup"><span data-stu-id="bb79c-127">INPUTS</span></span>

### <span data-ttu-id="bb79c-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bb79c-128">System.String</span></span>


## <span data-ttu-id="bb79c-129">출력</span><span class="sxs-lookup"><span data-stu-id="bb79c-129">OUTPUTS</span></span>

### <span data-ttu-id="bb79c-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="bb79c-130">System.Void</span></span>


## <span data-ttu-id="bb79c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="bb79c-131">NOTES</span></span>

## <span data-ttu-id="bb79c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb79c-132">RELATED LINKS</span></span>
