---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212700"
---
# <span data-ttu-id="ff727-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="ff727-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="ff727-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff727-102">SYNOPSIS</span></span>
<span data-ttu-id="ff727-103">지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff727-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="ff727-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff727-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff727-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ff727-105">DESCRIPTION</span></span>
<span data-ttu-id="ff727-106">**AzRelayNamespace** cmdlet은 지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff727-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="ff727-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ff727-107">EXAMPLES</span></span>

### <span data-ttu-id="ff727-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ff727-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="ff727-109">지정 된 리소스 그룹에서 릴레이 네임 스페이스를 제거 `TestNameSpace-Relay1` `Default-ServiceBus-WestUS` 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff727-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="ff727-110">변수</span><span class="sxs-lookup"><span data-stu-id="ff727-110">PARAMETERS</span></span>

### <span data-ttu-id="ff727-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff727-111">-DefaultProfile</span></span>
<span data-ttu-id="ff727-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff727-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff727-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ff727-113">-Name</span></span>
<span data-ttu-id="ff727-114">릴레이 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff727-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="ff727-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff727-115">-ResourceGroupName</span></span>
<span data-ttu-id="ff727-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff727-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="ff727-117">-확인</span><span class="sxs-lookup"><span data-stu-id="ff727-117">-Confirm</span></span>
<span data-ttu-id="ff727-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff727-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff727-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff727-119">-WhatIf</span></span>
<span data-ttu-id="ff727-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff727-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff727-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff727-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff727-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff727-122">CommonParameters</span></span>
<span data-ttu-id="ff727-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff727-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff727-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff727-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff727-125">입력</span><span class="sxs-lookup"><span data-stu-id="ff727-125">INPUTS</span></span>

### <span data-ttu-id="ff727-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff727-126">System.String</span></span>

## <span data-ttu-id="ff727-127">출력</span><span class="sxs-lookup"><span data-stu-id="ff727-127">OUTPUTS</span></span>

### <span data-ttu-id="ff727-128">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="ff727-128">System.Void</span></span>

## <span data-ttu-id="ff727-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ff727-129">NOTES</span></span>

## <span data-ttu-id="ff727-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff727-130">RELATED LINKS</span></span>
