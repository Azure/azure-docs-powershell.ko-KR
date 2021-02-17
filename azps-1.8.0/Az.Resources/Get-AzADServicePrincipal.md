---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 1b8a1c5c0a8161993be4d1e8c5f8d4bf9119d4b0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399705"
---
# <span data-ttu-id="4c7ff-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4c7ff-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="4c7ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="4c7ff-103">Active Directory 서비스 주체 필터</span><span class="sxs-lookup"><span data-stu-id="4c7ff-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="4c7ff-104">구문</span><span class="sxs-lookup"><span data-stu-id="4c7ff-104">SYNTAX</span></span>

### <span data-ttu-id="4c7ff-105">EmptyParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4c7ff-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4c7ff-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c7ff-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4c7ff-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c7ff-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4c7ff-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c7ff-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4c7ff-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c7ff-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4c7ff-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c7ff-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4c7ff-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c7ff-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="4c7ff-112">설명</span><span class="sxs-lookup"><span data-stu-id="4c7ff-112">DESCRIPTION</span></span>
<span data-ttu-id="4c7ff-113">Active Directory 서비스 주체 필터</span><span class="sxs-lookup"><span data-stu-id="4c7ff-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="4c7ff-114">예제</span><span class="sxs-lookup"><span data-stu-id="4c7ff-114">EXAMPLES</span></span>

### <span data-ttu-id="4c7ff-115">예제 1 - AD 서비스 주체 나열</span><span class="sxs-lookup"><span data-stu-id="4c7ff-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="4c7ff-116">테넌트의 모든 AD 서비스 주체가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="4c7ff-117">예제 2 - Paging를 사용하여 AD 서비스 주체 나열</span><span class="sxs-lookup"><span data-stu-id="4c7ff-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="4c7ff-118">테넌트에 처음 100개 AD 서비스 주체가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="4c7ff-119">예제 3 - SPN으로 서비스 주체 나열</span><span class="sxs-lookup"><span data-stu-id="4c7ff-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="4c7ff-120">SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'가 있는 서비스 주체 나열</span><span class="sxs-lookup"><span data-stu-id="4c7ff-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="4c7ff-121">예제 4 - 검색 문자열로 서비스 주체 나열</span><span class="sxs-lookup"><span data-stu-id="4c7ff-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="4c7ff-122">표시 이름이 "웹"으로 시작하는 모든 AD 서비스 주체가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="4c7ff-123">예제 5 - 파이핑을 통해 서비스 주체 나열</span><span class="sxs-lookup"><span data-stu-id="4c7ff-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="4c7ff-124">개체 ID가 '39e64ec6-569b-4030-8e1c-c3c519a05d69'인 AD 애플리케이션을 시작하고 Get-AzADServicePrincipal cmdlet에 파이프하여 해당 애플리케이션의 모든 서비스 주체 목록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="4c7ff-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c7ff-125">PARAMETERS</span></span>

### <span data-ttu-id="4c7ff-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4c7ff-126">-ApplicationId</span></span>
<span data-ttu-id="4c7ff-127">서비스 주체 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-127">The service principal application id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c7ff-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="4c7ff-128">-ApplicationObject</span></span>
<span data-ttu-id="4c7ff-129">서비스 주체가 검색되는 애플리케이션 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c7ff-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c7ff-130">-DefaultProfile</span></span>
<span data-ttu-id="4c7ff-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4c7ff-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c7ff-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4c7ff-132">-DisplayName</span></span>
<span data-ttu-id="4c7ff-133">서비스 주체 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-133">The service principal display name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c7ff-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="4c7ff-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="4c7ff-135">서비스 주체 검색 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-135">The service principal search string.</span></span>

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

### <span data-ttu-id="4c7ff-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4c7ff-136">-ObjectId</span></span>
<span data-ttu-id="4c7ff-137">서비스 주체의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-137">Object id of the service principal.</span></span>

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

### <span data-ttu-id="4c7ff-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="4c7ff-138">-ServicePrincipalName</span></span>
<span data-ttu-id="4c7ff-139">서비스의 SPN입니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-139">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c7ff-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="4c7ff-140">-IncludeTotalCount</span></span>
<span data-ttu-id="4c7ff-141">데이터 집합의 개체 수를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="4c7ff-142">현재 이 매개 변수는 아무 것도 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="4c7ff-143">-Skip</span><span class="sxs-lookup"><span data-stu-id="4c7ff-143">-Skip</span></span>
<span data-ttu-id="4c7ff-144">첫 번째 N개 개체를 무시하고 나머지 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="4c7ff-145">-First</span><span class="sxs-lookup"><span data-stu-id="4c7ff-145">-First</span></span>
<span data-ttu-id="4c7ff-146">반환할 개체의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="4c7ff-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c7ff-147">CommonParameters</span></span>
<span data-ttu-id="4c7ff-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c7ff-149">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4c7ff-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c7ff-150">입력</span><span class="sxs-lookup"><span data-stu-id="4c7ff-150">INPUTS</span></span>

### <span data-ttu-id="4c7ff-151">System.String</span><span class="sxs-lookup"><span data-stu-id="4c7ff-151">System.String</span></span>

### <span data-ttu-id="4c7ff-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4c7ff-152">System.Guid</span></span>

### <span data-ttu-id="4c7ff-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="4c7ff-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="4c7ff-154">출력</span><span class="sxs-lookup"><span data-stu-id="4c7ff-154">OUTPUTS</span></span>

### <span data-ttu-id="4c7ff-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4c7ff-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="4c7ff-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4c7ff-156">NOTES</span></span>

## <span data-ttu-id="4c7ff-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c7ff-157">RELATED LINKS</span></span>

[<span data-ttu-id="4c7ff-158">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4c7ff-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)


[<span data-ttu-id="4c7ff-159">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4c7ff-159">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="4c7ff-160">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="4c7ff-160">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="4c7ff-161">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4c7ff-161">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

