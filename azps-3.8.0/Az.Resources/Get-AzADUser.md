---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: d0391b47e4060b2b93206c8e4d2722ca682a0db4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879022"
---
# <span data-ttu-id="8e895-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="8e895-101">Get-AzADUser</span></span>

## <span data-ttu-id="8e895-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e895-102">SYNOPSIS</span></span>
<span data-ttu-id="8e895-103">Active directory 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-103">Filters active directory users.</span></span>

## <span data-ttu-id="8e895-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e895-104">SYNTAX</span></span>

### <span data-ttu-id="8e895-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8e895-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="8e895-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e895-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="8e895-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e895-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="8e895-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e895-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="8e895-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e895-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="8e895-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e895-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="8e895-111">설명은</span><span class="sxs-lookup"><span data-stu-id="8e895-111">DESCRIPTION</span></span>
<span data-ttu-id="8e895-112">Active directory 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-112">Filters active directory users.</span></span>

## <span data-ttu-id="8e895-113">예제의</span><span class="sxs-lookup"><span data-stu-id="8e895-113">EXAMPLES</span></span>

### <span data-ttu-id="8e895-114">예제 1-모든 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="8e895-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="8e895-115">테 넌 트에서 모든 광고 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="8e895-116">예제 2-페이징을 사용 하 여 모든 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="8e895-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="8e895-117">테 넌 트에서 첫 번째 100 광고 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="8e895-118">예제 3-사용자 계정 이름으로 광고 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="8e895-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="8e895-119">사용자 계정 이름이 "" 인 광고 사용자를 가져옵니다 foo@domain.com .</span><span class="sxs-lookup"><span data-stu-id="8e895-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="8e895-120">예제 4-검색 문자열 목록</span><span class="sxs-lookup"><span data-stu-id="8e895-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="8e895-121">표시 이름이 "Joe"로 시작 하는 모든 광고 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="8e895-122">변수</span><span class="sxs-lookup"><span data-stu-id="8e895-122">PARAMETERS</span></span>

### <span data-ttu-id="8e895-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e895-123">-DefaultProfile</span></span>
<span data-ttu-id="8e895-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8e895-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e895-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8e895-125">-DisplayName</span></span>
<span data-ttu-id="8e895-126">사용자의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-126">The display name of the user.</span></span>

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

### <span data-ttu-id="8e895-127">-메일</span><span class="sxs-lookup"><span data-stu-id="8e895-127">-Mail</span></span>
<span data-ttu-id="8e895-128">사용자 메일입니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-128">The user mail.</span></span>

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

### <span data-ttu-id="8e895-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8e895-129">-ObjectId</span></span>
<span data-ttu-id="8e895-130">사용자의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-130">Object id of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e895-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="8e895-131">-StartsWith</span></span>
<span data-ttu-id="8e895-132">제공 된 문자열로 시작 하는 사용자를 찾는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="8e895-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8e895-133">-UserPrincipalName</span></span>
<span data-ttu-id="8e895-134">사용자의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-134">UPN of the user.</span></span>

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

### <span data-ttu-id="8e895-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="8e895-135">-IncludeTotalCount</span></span>
<span data-ttu-id="8e895-136">데이터 집합의 개체 수를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="8e895-137">현재이 매개 변수는 아무런 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="8e895-138">-생략</span><span class="sxs-lookup"><span data-stu-id="8e895-138">-Skip</span></span>
<span data-ttu-id="8e895-139">첫 N 개 개체를 무시 하 고 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="8e895-140">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="8e895-140">-First</span></span>
<span data-ttu-id="8e895-141">반환할 최대 개체 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="8e895-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e895-142">CommonParameters</span></span>
<span data-ttu-id="8e895-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e895-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e895-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e895-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e895-145">입력</span><span class="sxs-lookup"><span data-stu-id="8e895-145">INPUTS</span></span>

### <span data-ttu-id="8e895-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8e895-146">System.String</span></span>

## <span data-ttu-id="8e895-147">출력</span><span class="sxs-lookup"><span data-stu-id="8e895-147">OUTPUTS</span></span>

### <span data-ttu-id="8e895-148">ActiveDirectory를 사용 하 여 명령을 이동할 때</span><span class="sxs-lookup"><span data-stu-id="8e895-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="8e895-149">상속자</span><span class="sxs-lookup"><span data-stu-id="8e895-149">NOTES</span></span>

## <span data-ttu-id="8e895-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e895-150">RELATED LINKS</span></span>

[<span data-ttu-id="8e895-151">새로운 AzADUser</span><span class="sxs-lookup"><span data-stu-id="8e895-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="8e895-152">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="8e895-152">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="8e895-153">제거-AzADUser</span><span class="sxs-lookup"><span data-stu-id="8e895-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
