---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: 843a510376e49a1416129d719c141d72ec80df35
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492397"
---
# <span data-ttu-id="bf0f5-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="bf0f5-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="bf0f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0f5-103">관리 그룹에서 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="bf0f5-104">구문</span><span class="sxs-lookup"><span data-stu-id="bf0f5-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf0f5-105">설명</span><span class="sxs-lookup"><span data-stu-id="bf0f5-105">DESCRIPTION</span></span>
<span data-ttu-id="bf0f5-106">**Remove-AzManagementGroupSubscription** cmdlet은 관리 그룹에서 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="bf0f5-107">예제</span><span class="sxs-lookup"><span data-stu-id="bf0f5-107">EXAMPLES</span></span>

### <span data-ttu-id="bf0f5-108">예제 1: 관리 그룹에서 구독 제거</span><span class="sxs-lookup"><span data-stu-id="bf0f5-108">Example 1: Remove Subscription from a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="bf0f5-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf0f5-109">PARAMETERS</span></span>

### <span data-ttu-id="bf0f5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0f5-110">-DefaultProfile</span></span>
<span data-ttu-id="bf0f5-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf0f5-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="bf0f5-112">-GroupName</span></span>
<span data-ttu-id="bf0f5-113">관리 그룹 ID</span><span class="sxs-lookup"><span data-stu-id="bf0f5-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0f5-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf0f5-114">-PassThru</span></span>
<span data-ttu-id="bf0f5-115">성공적인 `true` 실행 시 반환</span><span class="sxs-lookup"><span data-stu-id="bf0f5-115">Return `true` on successful execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0f5-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf0f5-116">-SubscriptionId</span></span>
<span data-ttu-id="bf0f5-117">관리와 연결된 구독의 구독 ID</span><span class="sxs-lookup"><span data-stu-id="bf0f5-117">Subscription Id of the subscription associated with the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0f5-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf0f5-118">-Confirm</span></span>
<span data-ttu-id="bf0f5-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf0f5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf0f5-120">-WhatIf</span></span>
<span data-ttu-id="bf0f5-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bf0f5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf0f5-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf0f5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0f5-123">CommonParameters</span></span>
<span data-ttu-id="bf0f5-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0f5-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0f5-126">입력</span><span class="sxs-lookup"><span data-stu-id="bf0f5-126">INPUTS</span></span>

### <span data-ttu-id="bf0f5-127">없음</span><span class="sxs-lookup"><span data-stu-id="bf0f5-127">None</span></span>

## <span data-ttu-id="bf0f5-128">출력</span><span class="sxs-lookup"><span data-stu-id="bf0f5-128">OUTPUTS</span></span>

### <span data-ttu-id="bf0f5-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf0f5-129">System.Boolean</span></span>

## <span data-ttu-id="bf0f5-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bf0f5-130">NOTES</span></span>

## <span data-ttu-id="bf0f5-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf0f5-131">RELATED LINKS</span></span>
