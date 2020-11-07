---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 34a00ed29d40d8824ac0f2d24f5275bb7c0a0164
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876497"
---
# <span data-ttu-id="cbec3-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="cbec3-101">Get-AzADUser</span></span>

## <span data-ttu-id="cbec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbec3-102">SYNOPSIS</span></span>
<span data-ttu-id="cbec3-103">Active directory 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-103">Filters active directory users.</span></span>

## <span data-ttu-id="cbec3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cbec3-104">SYNTAX</span></span>

### <span data-ttu-id="cbec3-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cbec3-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cbec3-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbec3-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cbec3-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbec3-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cbec3-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbec3-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cbec3-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbec3-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cbec3-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbec3-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="cbec3-111">설명은</span><span class="sxs-lookup"><span data-stu-id="cbec3-111">DESCRIPTION</span></span>
<span data-ttu-id="cbec3-112">Active directory 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-112">Filters active directory users.</span></span>

## <span data-ttu-id="cbec3-113">예제의</span><span class="sxs-lookup"><span data-stu-id="cbec3-113">EXAMPLES</span></span>

### <span data-ttu-id="cbec3-114">예제 1-모든 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="cbec3-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="cbec3-115">테 넌 트에서 모든 광고 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="cbec3-116">예제 2-페이징을 사용 하 여 모든 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="cbec3-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="cbec3-117">테 넌 트에서 첫 번째 100 광고 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="cbec3-118">예제 3-사용자 계정 이름으로 광고 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="cbec3-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="cbec3-119">사용자 계정 이름이 "" 인 광고 사용자를 가져옵니다 foo@domain.com .</span><span class="sxs-lookup"><span data-stu-id="cbec3-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="cbec3-120">예제 4-검색 문자열 목록</span><span class="sxs-lookup"><span data-stu-id="cbec3-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="cbec3-121">표시 이름이 "Joe"로 시작 하는 모든 광고 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="cbec3-122">변수</span><span class="sxs-lookup"><span data-stu-id="cbec3-122">PARAMETERS</span></span>

### <span data-ttu-id="cbec3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbec3-123">-DefaultProfile</span></span>
<span data-ttu-id="cbec3-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cbec3-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbec3-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cbec3-125">-DisplayName</span></span>
<span data-ttu-id="cbec3-126">사용자의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-126">The display name of the user.</span></span>

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

### <span data-ttu-id="cbec3-127">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="cbec3-127">-First</span></span>
<span data-ttu-id="cbec3-128">반환할 최대 개체 수입니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="cbec3-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="cbec3-129">-IncludeTotalCount</span></span>
<span data-ttu-id="cbec3-130">데이터 집합의 개체 수를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="cbec3-131">현재이 매개 변수는 아무런 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="cbec3-132">-메일</span><span class="sxs-lookup"><span data-stu-id="cbec3-132">-Mail</span></span>
<span data-ttu-id="cbec3-133">사용자 메일입니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-133">The user mail.</span></span>

```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbec3-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cbec3-134">-ObjectId</span></span>
<span data-ttu-id="cbec3-135">사용자의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-135">Object id of the user.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbec3-136">-생략</span><span class="sxs-lookup"><span data-stu-id="cbec3-136">-Skip</span></span>
<span data-ttu-id="cbec3-137">첫 N 개 개체를 무시 하 고 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="cbec3-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="cbec3-138">-StartsWith</span></span>
<span data-ttu-id="cbec3-139">제공 된 문자열로 시작 하는 사용자를 찾는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-139">Used to find users that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbec3-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cbec3-140">-UserPrincipalName</span></span>
<span data-ttu-id="cbec3-141">사용자의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-141">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbec3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbec3-142">CommonParameters</span></span>
<span data-ttu-id="cbec3-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbec3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbec3-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbec3-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbec3-145">입력</span><span class="sxs-lookup"><span data-stu-id="cbec3-145">INPUTS</span></span>

### <span data-ttu-id="cbec3-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cbec3-146">System.String</span></span>

### <span data-ttu-id="cbec3-147">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="cbec3-147">System.Guid</span></span>

## <span data-ttu-id="cbec3-148">출력</span><span class="sxs-lookup"><span data-stu-id="cbec3-148">OUTPUTS</span></span>

### <span data-ttu-id="cbec3-149">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Aduser</span><span class="sxs-lookup"><span data-stu-id="cbec3-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="cbec3-150">상속자</span><span class="sxs-lookup"><span data-stu-id="cbec3-150">NOTES</span></span>

## <span data-ttu-id="cbec3-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbec3-151">RELATED LINKS</span></span>

[<span data-ttu-id="cbec3-152">새로운 AzADUser</span><span class="sxs-lookup"><span data-stu-id="cbec3-152">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="cbec3-153">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="cbec3-153">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="cbec3-154">제거-AzADUser</span><span class="sxs-lookup"><span data-stu-id="cbec3-154">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

