---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 984b5ef9a1ff19142ef044e1f3c919f8fb2a3dce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048057"
---
# <span data-ttu-id="07732-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="07732-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="07732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07732-102">SYNOPSIS</span></span>
<span data-ttu-id="07732-103">현재 테 넌 트의 광고 그룹 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="07732-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="07732-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07732-104">SYNTAX</span></span>

### <span data-ttu-id="07732-105">ObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="07732-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="07732-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="07732-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="07732-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07732-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="07732-108">설명은</span><span class="sxs-lookup"><span data-stu-id="07732-108">DESCRIPTION</span></span>
<span data-ttu-id="07732-109">현재 테 넌 트의 광고 그룹 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="07732-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="07732-110">예제의</span><span class="sxs-lookup"><span data-stu-id="07732-110">EXAMPLES</span></span>

### <span data-ttu-id="07732-111">예제 1: 광고 그룹별 개체 id를 기준으로 구성원 나열</span><span class="sxs-lookup"><span data-stu-id="07732-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="07732-112">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 AD 그룹의 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="07732-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="07732-113">예제 2: 페이징을 사용 하 여 AD group 개체 id를 기준으로 구성원 나열</span><span class="sxs-lookup"><span data-stu-id="07732-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="07732-114">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 AD 그룹의 첫 번째 100 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="07732-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="07732-115">예제 3: 파이핑을 기준으로 멤버 목록 표시</span><span class="sxs-lookup"><span data-stu-id="07732-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="07732-116">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 광고 그룹을 가져오고이를 Get-AzADGroupMember cmdlet에 파이프 하 여 해당 그룹의 모든 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="07732-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="07732-117">변수</span><span class="sxs-lookup"><span data-stu-id="07732-117">PARAMETERS</span></span>

### <span data-ttu-id="07732-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07732-118">-DefaultProfile</span></span>
<span data-ttu-id="07732-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="07732-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07732-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="07732-120">-GroupDisplayName</span></span>
<span data-ttu-id="07732-121">그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07732-121">The display name of the group.</span></span>

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

### <span data-ttu-id="07732-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="07732-122">-GroupObject</span></span>
<span data-ttu-id="07732-123">구성원을 나열 하는 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="07732-123">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07732-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="07732-124">-GroupObjectId</span></span>
<span data-ttu-id="07732-125">그룹의 개체 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="07732-125">Object Id of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07732-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="07732-126">-IncludeTotalCount</span></span>
<span data-ttu-id="07732-127">데이터 집합의 개체 수를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="07732-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="07732-128">현재이 매개 변수는 아무런 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07732-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="07732-129">-생략</span><span class="sxs-lookup"><span data-stu-id="07732-129">-Skip</span></span>
<span data-ttu-id="07732-130">첫 N 개 개체를 무시 하 고 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07732-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="07732-131">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="07732-131">-First</span></span>
<span data-ttu-id="07732-132">반환할 최대 개체 수입니다.</span><span class="sxs-lookup"><span data-stu-id="07732-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="07732-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07732-133">CommonParameters</span></span>
<span data-ttu-id="07732-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07732-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07732-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="07732-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07732-136">입력</span><span class="sxs-lookup"><span data-stu-id="07732-136">INPUTS</span></span>

### <span data-ttu-id="07732-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="07732-137">System.String</span></span>

### <span data-ttu-id="07732-138">ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="07732-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="07732-139">출력</span><span class="sxs-lookup"><span data-stu-id="07732-139">OUTPUTS</span></span>

### <span data-ttu-id="07732-140">ActiveDirectory/. m m m 개체</span><span class="sxs-lookup"><span data-stu-id="07732-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="07732-141">상속자</span><span class="sxs-lookup"><span data-stu-id="07732-141">NOTES</span></span>

## <span data-ttu-id="07732-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07732-142">RELATED LINKS</span></span>

[<span data-ttu-id="07732-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="07732-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="07732-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="07732-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

