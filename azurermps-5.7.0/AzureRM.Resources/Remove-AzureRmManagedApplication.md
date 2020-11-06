---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
ms.openlocfilehash: 1b5288b2ce0e453221819e6a0b80e06b45245160
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526611"
---
# <span data-ttu-id="c1f41-101">Remove-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="c1f41-101">Remove-AzureRmManagedApplication</span></span>

## <span data-ttu-id="c1f41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1f41-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f41-103">관리 되는 응용 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="c1f41-103">Removes a managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1f41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c1f41-104">SYNTAX</span></span>

### <span data-ttu-id="c1f41-105">RemoveByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="c1f41-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1f41-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="c1f41-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1f41-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c1f41-107">DESCRIPTION</span></span>
<span data-ttu-id="c1f41-108">**AzureRmManagedApplication** cmdlet은 관리 되는 응용 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="c1f41-108">The **Remove-AzureRmManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="c1f41-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c1f41-109">EXAMPLES</span></span>

### <span data-ttu-id="c1f41-110">예제 1: 리소스 ID로 관리 되는 응용 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="c1f41-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzureRmManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="c1f41-111">첫 번째 명령은 Get-AzureRmManagedApplication cmdlet을 사용 하 여 myApp 라는 관리 되는 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-111">The first command gets a managed application named myApp by using the Get-AzureRmManagedApplication cmdlet.</span></span>
<span data-ttu-id="c1f41-112">명령이 $Application 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-112">The command stores it in the $Application variable.</span></span>

<span data-ttu-id="c1f41-113">두 번째 명령은 $Application의 **ResourceId** 속성으로 식별 되는 관리 되는 응용 프로그램을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="c1f41-114">변수</span><span class="sxs-lookup"><span data-stu-id="c1f41-114">PARAMETERS</span></span>

### <span data-ttu-id="c1f41-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c1f41-115">-ApiVersion</span></span>
<span data-ttu-id="c1f41-116">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c1f41-117">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f41-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f41-118">-DefaultProfile</span></span>
<span data-ttu-id="c1f41-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f41-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c1f41-120">-Force</span></span>
<span data-ttu-id="c1f41-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f41-122">-Id</span><span class="sxs-lookup"><span data-stu-id="c1f41-122">-Id</span></span>
<span data-ttu-id="c1f41-123">구독을 포함 하는 정규화 된 관리 되는 응용 프로그램 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="c1f41-124">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="c1f41-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1f41-125">-이름</span><span class="sxs-lookup"><span data-stu-id="c1f41-125">-Name</span></span>
<span data-ttu-id="c1f41-126">관리 되는 응용 프로그램 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-126">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1f41-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="c1f41-127">-Pre</span></span>
<span data-ttu-id="c1f41-128">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f41-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1f41-129">-ResourceGroupName</span></span>
<span data-ttu-id="c1f41-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1f41-131">-확인</span><span class="sxs-lookup"><span data-stu-id="c1f41-131">-Confirm</span></span>
<span data-ttu-id="c1f41-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f41-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1f41-133">-WhatIf</span></span>
<span data-ttu-id="c1f41-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1f41-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f41-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f41-136">CommonParameters</span></span>
<span data-ttu-id="c1f41-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1f41-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f41-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1f41-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f41-139">입력</span><span class="sxs-lookup"><span data-stu-id="c1f41-139">INPUTS</span></span>

### <span data-ttu-id="c1f41-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c1f41-140">System.String</span></span>

## <span data-ttu-id="c1f41-141">출력</span><span class="sxs-lookup"><span data-stu-id="c1f41-141">OUTPUTS</span></span>

### <span data-ttu-id="c1f41-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c1f41-142">System.Boolean</span></span>

## <span data-ttu-id="c1f41-143">상속자</span><span class="sxs-lookup"><span data-stu-id="c1f41-143">NOTES</span></span>

## <span data-ttu-id="c1f41-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1f41-144">RELATED LINKS</span></span>
