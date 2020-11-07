---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
ms.openlocfilehash: f790266f1e61446cb9d1c257929cf8b6e3ab25d3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881281"
---
# <span data-ttu-id="57049-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="57049-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="57049-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57049-102">SYNOPSIS</span></span>
<span data-ttu-id="57049-103">현재 테 넌 트의 광고 그룹 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="57049-103">Lists members of an AD group in the current tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57049-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57049-104">SYNTAX</span></span>

### <span data-ttu-id="57049-105">ObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="57049-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="57049-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="57049-106">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="57049-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57049-107">GroupObjectParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="57049-108">설명은</span><span class="sxs-lookup"><span data-stu-id="57049-108">DESCRIPTION</span></span>
<span data-ttu-id="57049-109">현재 테 넌 트의 광고 그룹 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="57049-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="57049-110">예제의</span><span class="sxs-lookup"><span data-stu-id="57049-110">EXAMPLES</span></span>

### <span data-ttu-id="57049-111">예제 1-광고 그룹별 구성원 목록 개체 id</span><span class="sxs-lookup"><span data-stu-id="57049-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="57049-112">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 AD 그룹의 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="57049-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="57049-113">예제 2-페이징을 사용 하 여 광고 그룹 개체 id를 기준으로 구성원 나열</span><span class="sxs-lookup"><span data-stu-id="57049-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="57049-114">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 AD 그룹의 첫 번째 100 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="57049-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="57049-115">예제 3-파이핑을 기준으로 멤버 목록 표시</span><span class="sxs-lookup"><span data-stu-id="57049-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzureRmADGroupMember
```

<span data-ttu-id="57049-116">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 광고 그룹을 가져오고이를 Get-AzureRmADGroupMember cmdlet에 파이프 하 여 해당 그룹의 모든 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="57049-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzureRmADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="57049-117">변수</span><span class="sxs-lookup"><span data-stu-id="57049-117">PARAMETERS</span></span>

### <span data-ttu-id="57049-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57049-118">-DefaultProfile</span></span>
<span data-ttu-id="57049-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="57049-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57049-120">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="57049-120">-First</span></span>
<span data-ttu-id="57049-121">반환할 최대 개체 수입니다.</span><span class="sxs-lookup"><span data-stu-id="57049-121">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57049-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="57049-122">-GroupDisplayName</span></span>
<span data-ttu-id="57049-123">그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57049-123">The display name of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57049-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="57049-124">-GroupObject</span></span>
<span data-ttu-id="57049-125">구성원을 나열 하는 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="57049-125">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57049-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="57049-126">-GroupObjectId</span></span>
<span data-ttu-id="57049-127">그룹의 개체 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="57049-127">Object Id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57049-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="57049-128">-IncludeTotalCount</span></span>
<span data-ttu-id="57049-129">데이터 집합의 개체 수를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="57049-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="57049-130">현재이 매개 변수는 아무런 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57049-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="57049-131">-생략</span><span class="sxs-lookup"><span data-stu-id="57049-131">-Skip</span></span>
<span data-ttu-id="57049-132">첫 N 개 개체를 무시 하 고 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57049-132">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57049-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57049-133">CommonParameters</span></span>
<span data-ttu-id="57049-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57049-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57049-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57049-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57049-136">입력</span><span class="sxs-lookup"><span data-stu-id="57049-136">INPUTS</span></span>

### <span data-ttu-id="57049-137">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="57049-137">System.Guid</span></span>

### <span data-ttu-id="57049-138">Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="57049-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="57049-139">매개 변수: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="57049-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="57049-140">출력</span><span class="sxs-lookup"><span data-stu-id="57049-140">OUTPUTS</span></span>

### <span data-ttu-id="57049-141">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Ad개체</span><span class="sxs-lookup"><span data-stu-id="57049-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="57049-142">상속자</span><span class="sxs-lookup"><span data-stu-id="57049-142">NOTES</span></span>

## <span data-ttu-id="57049-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57049-143">RELATED LINKS</span></span>

[<span data-ttu-id="57049-144">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="57049-144">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="57049-145">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="57049-145">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

