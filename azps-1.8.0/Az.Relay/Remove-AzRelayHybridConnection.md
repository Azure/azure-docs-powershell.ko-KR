---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: b0d7ef4a3fcaf681ea52719a5c7627784dac8d65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699502"
---
# <span data-ttu-id="d0dc3-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="d0dc3-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="d0dc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="d0dc3-103">지정 된 HybridConnection 네임 스페이스에서 HybridConnection를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0dc3-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="d0dc3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0dc3-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0dc3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d0dc3-105">DESCRIPTION</span></span>
<span data-ttu-id="d0dc3-106">**Remove-AzRelayHybridConnection** cmdlet은 지정 된 릴레이 네임 스페이스에서 HybridConnection를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0dc3-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="d0dc3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d0dc3-107">EXAMPLES</span></span>

### <span data-ttu-id="d0dc3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d0dc3-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="d0dc3-109">네임 스페이스에서 HybridConnection를 제거 합니다 `TestHybridConnection` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="d0dc3-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="d0dc3-110">변수</span><span class="sxs-lookup"><span data-stu-id="d0dc3-110">PARAMETERS</span></span>

### <span data-ttu-id="d0dc3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0dc3-111">-DefaultProfile</span></span>
<span data-ttu-id="d0dc3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0dc3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0dc3-113">-이름</span><span class="sxs-lookup"><span data-stu-id="d0dc3-113">-Name</span></span>
<span data-ttu-id="d0dc3-114">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0dc3-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="d0dc3-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d0dc3-115">-Namespace</span></span>
<span data-ttu-id="d0dc3-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0dc3-116">Namespace Name.</span></span>

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

### <span data-ttu-id="d0dc3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0dc3-117">-ResourceGroupName</span></span>
<span data-ttu-id="d0dc3-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0dc3-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="d0dc3-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d0dc3-119">-Confirm</span></span>
<span data-ttu-id="d0dc3-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0dc3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0dc3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0dc3-121">-WhatIf</span></span>
<span data-ttu-id="d0dc3-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0dc3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0dc3-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0dc3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0dc3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0dc3-124">CommonParameters</span></span>
<span data-ttu-id="d0dc3-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0dc3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0dc3-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0dc3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0dc3-127">입력</span><span class="sxs-lookup"><span data-stu-id="d0dc3-127">INPUTS</span></span>

### <span data-ttu-id="d0dc3-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d0dc3-128">System.String</span></span>

## <span data-ttu-id="d0dc3-129">출력</span><span class="sxs-lookup"><span data-stu-id="d0dc3-129">OUTPUTS</span></span>

### <span data-ttu-id="d0dc3-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d0dc3-130">System.Void</span></span>

## <span data-ttu-id="d0dc3-131">상속자</span><span class="sxs-lookup"><span data-stu-id="d0dc3-131">NOTES</span></span>

## <span data-ttu-id="d0dc3-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0dc3-132">RELATED LINKS</span></span>
