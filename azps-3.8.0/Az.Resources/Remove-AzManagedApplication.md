---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034257"
---
# <span data-ttu-id="b29da-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="b29da-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="b29da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b29da-102">SYNOPSIS</span></span>
<span data-ttu-id="b29da-103">관리 되는 응용 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="b29da-103">Removes a managed application</span></span>

## <span data-ttu-id="b29da-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b29da-104">SYNTAX</span></span>

### <span data-ttu-id="b29da-105">RemoveByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="b29da-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b29da-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="b29da-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b29da-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b29da-107">DESCRIPTION</span></span>
<span data-ttu-id="b29da-108">**AzManagedApplication** cmdlet은 관리 되는 응용 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="b29da-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="b29da-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b29da-109">EXAMPLES</span></span>

### <span data-ttu-id="b29da-110">예제 1: 리소스 ID로 관리 되는 응용 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="b29da-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="b29da-111">첫 번째 명령은 Get-AzManagedApplication cmdlet을 사용 하 여 myApp 라는 관리 되는 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="b29da-112">명령이 $Application 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="b29da-113">두 번째 명령은 $Application의 **ResourceId** 속성으로 식별 되는 관리 되는 응용 프로그램을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="b29da-114">변수</span><span class="sxs-lookup"><span data-stu-id="b29da-114">PARAMETERS</span></span>

### <span data-ttu-id="b29da-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b29da-115">-ApiVersion</span></span>
<span data-ttu-id="b29da-116">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b29da-117">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b29da-118">-DefaultProfile</span></span>
<span data-ttu-id="b29da-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b29da-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b29da-120">-Force</span></span>
<span data-ttu-id="b29da-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b29da-122">-Id</span><span class="sxs-lookup"><span data-stu-id="b29da-122">-Id</span></span>
<span data-ttu-id="b29da-123">구독을 포함 하는 정규화 된 관리 되는 응용 프로그램 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="b29da-124">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b29da-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b29da-125">-이름</span><span class="sxs-lookup"><span data-stu-id="b29da-125">-Name</span></span>
<span data-ttu-id="b29da-126">관리 되는 응용 프로그램 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b29da-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="b29da-127">-Pre</span></span>
<span data-ttu-id="b29da-128">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b29da-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b29da-129">-ResourceGroupName</span></span>
<span data-ttu-id="b29da-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b29da-131">-확인</span><span class="sxs-lookup"><span data-stu-id="b29da-131">-Confirm</span></span>
<span data-ttu-id="b29da-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b29da-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b29da-133">-WhatIf</span></span>
<span data-ttu-id="b29da-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b29da-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b29da-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b29da-136">CommonParameters</span></span>
<span data-ttu-id="b29da-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b29da-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b29da-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b29da-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b29da-139">입력</span><span class="sxs-lookup"><span data-stu-id="b29da-139">INPUTS</span></span>

### <span data-ttu-id="b29da-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b29da-140">System.String</span></span>

## <span data-ttu-id="b29da-141">출력</span><span class="sxs-lookup"><span data-stu-id="b29da-141">OUTPUTS</span></span>

### <span data-ttu-id="b29da-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b29da-142">System.Boolean</span></span>

## <span data-ttu-id="b29da-143">상속자</span><span class="sxs-lookup"><span data-stu-id="b29da-143">NOTES</span></span>

## <span data-ttu-id="b29da-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b29da-144">RELATED LINKS</span></span>
