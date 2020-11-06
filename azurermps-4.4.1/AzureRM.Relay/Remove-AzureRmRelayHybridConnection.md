---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7f65f77d9d1f525dd8850c6934263b608d241751
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533875"
---
# <span data-ttu-id="fd382-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="fd382-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="fd382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd382-102">SYNOPSIS</span></span>
<span data-ttu-id="fd382-103">지정 된 HybridConnection 네임 스페이스에서 HybridConnection를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd382-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd382-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd382-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd382-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fd382-105">DESCRIPTION</span></span>
<span data-ttu-id="fd382-106">**Remove-AzureRmRelayHybridConnection** cmdlet은 지정 된 릴레이 네임 스페이스에서 HybridConnection를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd382-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="fd382-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fd382-107">EXAMPLES</span></span>

### <span data-ttu-id="fd382-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fd382-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="fd382-109">네임 스페이스에서 HybridConnection를 제거 합니다 `TestHybridConnection` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="fd382-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="fd382-110">변수</span><span class="sxs-lookup"><span data-stu-id="fd382-110">PARAMETERS</span></span>

### <span data-ttu-id="fd382-111">-이름</span><span class="sxs-lookup"><span data-stu-id="fd382-111">-Name</span></span>
<span data-ttu-id="fd382-112">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd382-112">HybridConnections Name.</span></span>

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

### <span data-ttu-id="fd382-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fd382-113">-Namespace</span></span>
<span data-ttu-id="fd382-114">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd382-114">Namespace Name.</span></span>

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

### <span data-ttu-id="fd382-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd382-115">-ResourceGroupName</span></span>
<span data-ttu-id="fd382-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd382-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="fd382-117">-확인</span><span class="sxs-lookup"><span data-stu-id="fd382-117">-Confirm</span></span>
<span data-ttu-id="fd382-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd382-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd382-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd382-119">-WhatIf</span></span>
<span data-ttu-id="fd382-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd382-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd382-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd382-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd382-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd382-122">-DefaultProfile</span></span>
<span data-ttu-id="fd382-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd382-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd382-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd382-124">CommonParameters</span></span>
<span data-ttu-id="fd382-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd382-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd382-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd382-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd382-127">입력</span><span class="sxs-lookup"><span data-stu-id="fd382-127">INPUTS</span></span>

### <span data-ttu-id="fd382-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd382-128">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="fd382-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fd382-129">-Namespace</span></span>
    System.String

### <span data-ttu-id="fd382-130">-이름</span><span class="sxs-lookup"><span data-stu-id="fd382-130">-Name</span></span>
    System.String

## <span data-ttu-id="fd382-131">출력</span><span class="sxs-lookup"><span data-stu-id="fd382-131">OUTPUTS</span></span>

### <span data-ttu-id="fd382-132">System. 개체</span><span class="sxs-lookup"><span data-stu-id="fd382-132">System.Object</span></span>

## <span data-ttu-id="fd382-133">상속자</span><span class="sxs-lookup"><span data-stu-id="fd382-133">NOTES</span></span>

## <span data-ttu-id="fd382-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd382-134">RELATED LINKS</span></span>

