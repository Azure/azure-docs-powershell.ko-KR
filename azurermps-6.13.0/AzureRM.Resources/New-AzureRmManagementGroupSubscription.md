---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroupSubscription.md
ms.openlocfilehash: a3c75c653d75a4fde969672a245644ee04412731
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524280"
---
# <span data-ttu-id="3bd5c-101">New-AzureRmManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="3bd5c-101">New-AzureRmManagementGroupSubscription</span></span>

## <span data-ttu-id="3bd5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bd5c-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd5c-103">관리 그룹에 구독을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd5c-103">Adds a Subscription to a Management Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bd5c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3bd5c-104">SYNTAX</span></span>

```
New-AzureRmManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bd5c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3bd5c-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd5c-106">**새 AzureRMManagementGroupSubscription** Cmdlet은 관리 그룹에 구독을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd5c-106">The **New-AzureRMManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="3bd5c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3bd5c-107">EXAMPLES</span></span>

### <span data-ttu-id="3bd5c-108">예제 1: 관리 그룹에 구독 추가</span><span class="sxs-lookup"><span data-stu-id="3bd5c-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzureRMManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="3bd5c-109">변수</span><span class="sxs-lookup"><span data-stu-id="3bd5c-109">PARAMETERS</span></span>

### <span data-ttu-id="3bd5c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd5c-110">-DefaultProfile</span></span>
<span data-ttu-id="3bd5c-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3bd5c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bd5c-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="3bd5c-112">-GroupName</span></span>
<span data-ttu-id="3bd5c-113">관리 그룹 Id</span><span class="sxs-lookup"><span data-stu-id="3bd5c-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd5c-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bd5c-114">-PassThru</span></span>
<span data-ttu-id="3bd5c-115">성공적으로 실행 되는 경우 반환 `true`</span><span class="sxs-lookup"><span data-stu-id="3bd5c-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="3bd5c-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3bd5c-116">-SubscriptionId</span></span>
<span data-ttu-id="3bd5c-117">관리에 연결 된 구독의 구독 Id</span><span class="sxs-lookup"><span data-stu-id="3bd5c-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="3bd5c-118">-확인</span><span class="sxs-lookup"><span data-stu-id="3bd5c-118">-Confirm</span></span>
<span data-ttu-id="3bd5c-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd5c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bd5c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd5c-120">-WhatIf</span></span>
<span data-ttu-id="3bd5c-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3bd5c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bd5c-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3bd5c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd5c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd5c-123">CommonParameters</span></span>
<span data-ttu-id="3bd5c-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd5c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd5c-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bd5c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd5c-126">입력</span><span class="sxs-lookup"><span data-stu-id="3bd5c-126">INPUTS</span></span>

### <span data-ttu-id="3bd5c-127">않아야</span><span class="sxs-lookup"><span data-stu-id="3bd5c-127">None</span></span>

## <span data-ttu-id="3bd5c-128">출력</span><span class="sxs-lookup"><span data-stu-id="3bd5c-128">OUTPUTS</span></span>

### <span data-ttu-id="3bd5c-129">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3bd5c-129">System.Boolean</span></span>

## <span data-ttu-id="3bd5c-130">상속자</span><span class="sxs-lookup"><span data-stu-id="3bd5c-130">NOTES</span></span>

## <span data-ttu-id="3bd5c-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3bd5c-131">RELATED LINKS</span></span>
