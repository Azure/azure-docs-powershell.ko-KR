---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: b19571025aeb6349277e9ae366146774862e8a80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702585"
---
# <span data-ttu-id="a4b09-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a4b09-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="a4b09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4b09-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b09-103">Active directory 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4b09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a4b09-104">SYNTAX</span></span>

### <span data-ttu-id="a4b09-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a4b09-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a4b09-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4b09-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a4b09-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4b09-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a4b09-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4b09-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a4b09-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4b09-109">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a4b09-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4b09-110">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="a4b09-111">설명은</span><span class="sxs-lookup"><span data-stu-id="a4b09-111">DESCRIPTION</span></span>
<span data-ttu-id="a4b09-112">Active directory 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-112">Filters active directory users.</span></span>

## <span data-ttu-id="a4b09-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a4b09-113">EXAMPLES</span></span>

### <span data-ttu-id="a4b09-114">예제 1-모든 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="a4b09-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="a4b09-115">테 넌 트에서 모든 광고 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="a4b09-116">예제 2-페이징을 사용 하 여 모든 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="a4b09-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzureRmADUser -First 100
```

<span data-ttu-id="a4b09-117">테 넌 트에서 첫 번째 100 광고 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="a4b09-118">예제 3-사용자 계정 이름으로 광고 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="a4b09-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="a4b09-119">사용자 계정 이름이 "" 인 광고 사용자를 가져옵니다 foo@domain.com .</span><span class="sxs-lookup"><span data-stu-id="a4b09-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="a4b09-120">예제 4-검색 문자열 목록</span><span class="sxs-lookup"><span data-stu-id="a4b09-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="a4b09-121">표시 이름이 "Joe"로 시작 하는 모든 광고 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="a4b09-122">변수</span><span class="sxs-lookup"><span data-stu-id="a4b09-122">PARAMETERS</span></span>

### <span data-ttu-id="a4b09-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b09-123">-DefaultProfile</span></span>
<span data-ttu-id="a4b09-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a4b09-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4b09-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a4b09-125">-DisplayName</span></span>
<span data-ttu-id="a4b09-126">사용자의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-126">The display name of the user.</span></span>

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

### <span data-ttu-id="a4b09-127">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="a4b09-127">-First</span></span>
<span data-ttu-id="a4b09-128">반환할 최대 개체 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="a4b09-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="a4b09-129">-IncludeTotalCount</span></span>
<span data-ttu-id="a4b09-130">데이터 집합의 개체 수를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="a4b09-131">현재이 매개 변수는 아무런 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="a4b09-132">-메일</span><span class="sxs-lookup"><span data-stu-id="a4b09-132">-Mail</span></span>
<span data-ttu-id="a4b09-133">사용자 메일입니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-133">The user mail.</span></span>

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

### <span data-ttu-id="a4b09-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a4b09-134">-ObjectId</span></span>
<span data-ttu-id="a4b09-135">사용자의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-135">Object id of the user.</span></span>

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

### <span data-ttu-id="a4b09-136">-생략</span><span class="sxs-lookup"><span data-stu-id="a4b09-136">-Skip</span></span>
<span data-ttu-id="a4b09-137">첫 N 개 개체를 무시 하 고 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="a4b09-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="a4b09-138">-StartsWith</span></span>
<span data-ttu-id="a4b09-139">제공 된 문자열로 시작 하는 사용자를 찾는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="a4b09-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a4b09-140">-UserPrincipalName</span></span>
<span data-ttu-id="a4b09-141">사용자의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-141">UPN of the user.</span></span>

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

### <span data-ttu-id="a4b09-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b09-142">CommonParameters</span></span>
<span data-ttu-id="a4b09-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4b09-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b09-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4b09-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b09-145">입력</span><span class="sxs-lookup"><span data-stu-id="a4b09-145">INPUTS</span></span>

### <span data-ttu-id="a4b09-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a4b09-146">System.String</span></span>

### <span data-ttu-id="a4b09-147">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="a4b09-147">System.Guid</span></span>

## <span data-ttu-id="a4b09-148">출력</span><span class="sxs-lookup"><span data-stu-id="a4b09-148">OUTPUTS</span></span>

### <span data-ttu-id="a4b09-149">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Aduser</span><span class="sxs-lookup"><span data-stu-id="a4b09-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="a4b09-150">상속자</span><span class="sxs-lookup"><span data-stu-id="a4b09-150">NOTES</span></span>

## <span data-ttu-id="a4b09-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4b09-151">RELATED LINKS</span></span>

[<span data-ttu-id="a4b09-152">새로운 AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a4b09-152">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="a4b09-153">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a4b09-153">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="a4b09-154">제거-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a4b09-154">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

