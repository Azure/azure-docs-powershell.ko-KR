---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: 30d13f9a5f9338a33f8ec6f6aaba9b40e028f087
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967659"
---
# <span data-ttu-id="f1a3f-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="f1a3f-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="f1a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a3f-103">관리 그룹에서 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a3f-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="f1a3f-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1a3f-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a3f-105">설명</span><span class="sxs-lookup"><span data-stu-id="f1a3f-105">DESCRIPTION</span></span>
<span data-ttu-id="f1a3f-106">**Remove-AzManagementGroupSubscription** cmdlet은 관리 그룹에서 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a3f-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="f1a3f-107">예제</span><span class="sxs-lookup"><span data-stu-id="f1a3f-107">EXAMPLES</span></span>

### <span data-ttu-id="f1a3f-108">예제 1: 관리 그룹에서 구독 제거</span><span class="sxs-lookup"><span data-stu-id="f1a3f-108">Example 1: Remove Subscription from a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="f1a3f-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f1a3f-109">PARAMETERS</span></span>

### <span data-ttu-id="f1a3f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a3f-110">-DefaultProfile</span></span>
<span data-ttu-id="f1a3f-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a3f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1a3f-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="f1a3f-112">-GroupName</span></span>
<span data-ttu-id="f1a3f-113">관리 그룹 ID</span><span class="sxs-lookup"><span data-stu-id="f1a3f-113">Management Group Id</span></span>

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

### <span data-ttu-id="f1a3f-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1a3f-114">-PassThru</span></span>
<span data-ttu-id="f1a3f-115">성공적인 `true` 실행에 대한 반환</span><span class="sxs-lookup"><span data-stu-id="f1a3f-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="f1a3f-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1a3f-116">-SubscriptionId</span></span>
<span data-ttu-id="f1a3f-117">관리와 연결된 구독의 구독 ID</span><span class="sxs-lookup"><span data-stu-id="f1a3f-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="f1a3f-118">-확인</span><span class="sxs-lookup"><span data-stu-id="f1a3f-118">-Confirm</span></span>
<span data-ttu-id="f1a3f-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1a3f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a3f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a3f-120">-WhatIf</span></span>
<span data-ttu-id="f1a3f-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1a3f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a3f-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1a3f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a3f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a3f-123">CommonParameters</span></span>
<span data-ttu-id="f1a3f-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a3f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a3f-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1a3f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a3f-126">입력</span><span class="sxs-lookup"><span data-stu-id="f1a3f-126">INPUTS</span></span>

### <span data-ttu-id="f1a3f-127">없음</span><span class="sxs-lookup"><span data-stu-id="f1a3f-127">None</span></span>

## <span data-ttu-id="f1a3f-128">출력</span><span class="sxs-lookup"><span data-stu-id="f1a3f-128">OUTPUTS</span></span>

### <span data-ttu-id="f1a3f-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1a3f-129">System.Boolean</span></span>

## <span data-ttu-id="f1a3f-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1a3f-130">NOTES</span></span>

## <span data-ttu-id="f1a3f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1a3f-131">RELATED LINKS</span></span>
