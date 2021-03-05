---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 17a5cb5c05b9bd3293b15ef48b90c8d7387744da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000459"
---
# <span data-ttu-id="0ec70-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="0ec70-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="0ec70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ec70-102">SYNOPSIS</span></span>
<span data-ttu-id="0ec70-103">지정된 리소스 그룹에서 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0ec70-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="0ec70-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ec70-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ec70-105">설명</span><span class="sxs-lookup"><span data-stu-id="0ec70-105">DESCRIPTION</span></span>
<span data-ttu-id="0ec70-106">**Remove-AzRelayNamespace** cmdlet은 지정된 리소스 그룹에서 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0ec70-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="0ec70-107">예제</span><span class="sxs-lookup"><span data-stu-id="0ec70-107">EXAMPLES</span></span>

### <span data-ttu-id="0ec70-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0ec70-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="0ec70-109">지정된 리소스 그룹에서 릴레이 `TestNameSpace-Relay1` 네임스페이스를 `Default-ServiceBus-WestUS` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0ec70-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="0ec70-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ec70-110">PARAMETERS</span></span>

### <span data-ttu-id="0ec70-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ec70-111">-DefaultProfile</span></span>
<span data-ttu-id="0ec70-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ec70-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ec70-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0ec70-113">-Name</span></span>
<span data-ttu-id="0ec70-114">릴레이 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ec70-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="0ec70-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ec70-115">-ResourceGroupName</span></span>
<span data-ttu-id="0ec70-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ec70-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="0ec70-117">-확인</span><span class="sxs-lookup"><span data-stu-id="0ec70-117">-Confirm</span></span>
<span data-ttu-id="0ec70-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ec70-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ec70-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ec70-119">-WhatIf</span></span>
<span data-ttu-id="0ec70-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ec70-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ec70-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ec70-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ec70-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ec70-122">CommonParameters</span></span>
<span data-ttu-id="0ec70-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ec70-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ec70-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0ec70-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ec70-125">입력</span><span class="sxs-lookup"><span data-stu-id="0ec70-125">INPUTS</span></span>

### <span data-ttu-id="0ec70-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0ec70-126">System.String</span></span>

## <span data-ttu-id="0ec70-127">출력</span><span class="sxs-lookup"><span data-stu-id="0ec70-127">OUTPUTS</span></span>

### <span data-ttu-id="0ec70-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="0ec70-128">System.Void</span></span>

## <span data-ttu-id="0ec70-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ec70-129">NOTES</span></span>

## <span data-ttu-id="0ec70-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ec70-130">RELATED LINKS</span></span>
