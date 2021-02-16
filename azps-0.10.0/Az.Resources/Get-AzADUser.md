---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: b5690dfc1d85483b10fc7cd08606c4555784e8e0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398736"
---
# <span data-ttu-id="bb128-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="bb128-101">Get-AzADUser</span></span>

## <span data-ttu-id="bb128-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb128-102">SYNOPSIS</span></span>
<span data-ttu-id="bb128-103">Active Directory 사용자를 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-103">Filters active directory users.</span></span>

## <span data-ttu-id="bb128-104">구문</span><span class="sxs-lookup"><span data-stu-id="bb128-104">SYNTAX</span></span>

### <span data-ttu-id="bb128-105">EmptyParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bb128-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="bb128-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb128-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="bb128-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb128-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="bb128-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb128-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="bb128-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb128-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="bb128-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb128-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="bb128-111">설명</span><span class="sxs-lookup"><span data-stu-id="bb128-111">DESCRIPTION</span></span>
<span data-ttu-id="bb128-112">Active Directory 사용자를 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-112">Filters active directory users.</span></span>

## <span data-ttu-id="bb128-113">예제</span><span class="sxs-lookup"><span data-stu-id="bb128-113">EXAMPLES</span></span>

### <span data-ttu-id="bb128-114">예제 1 - 모든 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="bb128-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="bb128-115">테넌트의 모든 AD 사용자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="bb128-116">예제 2 - Paging를 사용하여 모든 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="bb128-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="bb128-117">테넌트의 처음 100명 AD 사용자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="bb128-118">예제 3 - 사용자 계정 이름으로 AD 사용자 얻기</span><span class="sxs-lookup"><span data-stu-id="bb128-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="bb128-119">사용자 계정 이름 " "을(를) 통해 AD 사용자를 foo@domain.com 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="bb128-120">예제 4 - 검색 문자열로 나열</span><span class="sxs-lookup"><span data-stu-id="bb128-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="bb128-121">표시 이름이 "Joe"로 시작하는 모든 AD 사용자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="bb128-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb128-122">PARAMETERS</span></span>

### <span data-ttu-id="bb128-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb128-123">-DefaultProfile</span></span>
<span data-ttu-id="bb128-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bb128-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb128-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bb128-125">-DisplayName</span></span>
<span data-ttu-id="bb128-126">사용자의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-126">The display name of the user.</span></span>

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

### <span data-ttu-id="bb128-127">-First</span><span class="sxs-lookup"><span data-stu-id="bb128-127">-First</span></span>
<span data-ttu-id="bb128-128">반환할 개체의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="bb128-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="bb128-129">-IncludeTotalCount</span></span>
<span data-ttu-id="bb128-130">데이터 집합의 개체 수를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="bb128-131">현재 이 매개 변수는 아무 것도 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="bb128-132">-Mail</span><span class="sxs-lookup"><span data-stu-id="bb128-132">-Mail</span></span>
<span data-ttu-id="bb128-133">사용자 메일입니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-133">The user mail.</span></span>

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

### <span data-ttu-id="bb128-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bb128-134">-ObjectId</span></span>
<span data-ttu-id="bb128-135">사용자의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-135">Object id of the user.</span></span>

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

### <span data-ttu-id="bb128-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="bb128-136">-Skip</span></span>
<span data-ttu-id="bb128-137">첫 번째 N개 개체를 무시하고 나머지 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="bb128-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="bb128-138">-StartsWith</span></span>
<span data-ttu-id="bb128-139">제공된 문자열로 시작하는 사용자를 찾는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="bb128-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bb128-140">-UserPrincipalName</span></span>
<span data-ttu-id="bb128-141">사용자의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-141">UPN of the user.</span></span>

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

### <span data-ttu-id="bb128-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb128-142">CommonParameters</span></span>
<span data-ttu-id="bb128-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bb128-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb128-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bb128-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb128-145">입력</span><span class="sxs-lookup"><span data-stu-id="bb128-145">INPUTS</span></span>

### <span data-ttu-id="bb128-146">System.String</span><span class="sxs-lookup"><span data-stu-id="bb128-146">System.String</span></span>

### <span data-ttu-id="bb128-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="bb128-147">System.Guid</span></span>

## <span data-ttu-id="bb128-148">출력</span><span class="sxs-lookup"><span data-stu-id="bb128-148">OUTPUTS</span></span>

### <span data-ttu-id="bb128-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="bb128-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="bb128-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bb128-150">NOTES</span></span>

## <span data-ttu-id="bb128-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb128-151">RELATED LINKS</span></span>

[<span data-ttu-id="bb128-152">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="bb128-152">New-AzADUser</span></span>](./New-AzADUser.md)


[<span data-ttu-id="bb128-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="bb128-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

