---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: 238c4ecf92cbdd1dc6e9e0a430ec8e6ad200b967
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201945"
---
# <span data-ttu-id="5ba27-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="5ba27-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="5ba27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ba27-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba27-103">지정된 Relay 네임스페이스에서 WcfRelay를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba27-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="5ba27-104">구문</span><span class="sxs-lookup"><span data-stu-id="5ba27-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ba27-105">설명</span><span class="sxs-lookup"><span data-stu-id="5ba27-105">DESCRIPTION</span></span>
<span data-ttu-id="5ba27-106">**Remove-AzWcfRelay** cmdlet은 지정된 Relay 네임스페이스에서 WcfRelay를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba27-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="5ba27-107">예제</span><span class="sxs-lookup"><span data-stu-id="5ba27-107">EXAMPLES</span></span>

### <span data-ttu-id="5ba27-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ba27-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="5ba27-109">네임스페이스에서 WcfRelay를 `TestWCFRelay1` `TestNameSpace-Relay1` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba27-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="5ba27-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ba27-110">PARAMETERS</span></span>

### <span data-ttu-id="5ba27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba27-111">-DefaultProfile</span></span>
<span data-ttu-id="5ba27-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba27-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ba27-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5ba27-113">-Name</span></span>
<span data-ttu-id="5ba27-114">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba27-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="5ba27-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5ba27-115">-Namespace</span></span>
<span data-ttu-id="5ba27-116">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba27-116">Namespace Name.</span></span>

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

### <span data-ttu-id="5ba27-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba27-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ba27-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba27-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="5ba27-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ba27-119">-Confirm</span></span>
<span data-ttu-id="5ba27-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ba27-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ba27-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ba27-121">-WhatIf</span></span>
<span data-ttu-id="5ba27-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5ba27-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ba27-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5ba27-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ba27-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba27-124">CommonParameters</span></span>
<span data-ttu-id="5ba27-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba27-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba27-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5ba27-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba27-127">입력</span><span class="sxs-lookup"><span data-stu-id="5ba27-127">INPUTS</span></span>

### <span data-ttu-id="5ba27-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5ba27-128">System.String</span></span>

## <span data-ttu-id="5ba27-129">출력</span><span class="sxs-lookup"><span data-stu-id="5ba27-129">OUTPUTS</span></span>

### <span data-ttu-id="5ba27-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="5ba27-130">System.Void</span></span>

## <span data-ttu-id="5ba27-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5ba27-131">NOTES</span></span>

## <span data-ttu-id="5ba27-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ba27-132">RELATED LINKS</span></span>
