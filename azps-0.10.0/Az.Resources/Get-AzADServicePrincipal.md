---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 01f6b6d6ed119945af7d99bac9227c788976cbab
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398702"
---
# <span data-ttu-id="db2c6-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="db2c6-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="db2c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db2c6-102">SYNOPSIS</span></span>
<span data-ttu-id="db2c6-103">Active Directory 서비스 주체 필터</span><span class="sxs-lookup"><span data-stu-id="db2c6-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="db2c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="db2c6-104">SYNTAX</span></span>

### <span data-ttu-id="db2c6-105">EmptyParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="db2c6-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="db2c6-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c6-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="db2c6-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c6-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="db2c6-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c6-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="db2c6-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c6-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="db2c6-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c6-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="db2c6-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2c6-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="db2c6-112">설명</span><span class="sxs-lookup"><span data-stu-id="db2c6-112">DESCRIPTION</span></span>
<span data-ttu-id="db2c6-113">Active Directory 서비스 주체 필터</span><span class="sxs-lookup"><span data-stu-id="db2c6-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="db2c6-114">예제</span><span class="sxs-lookup"><span data-stu-id="db2c6-114">EXAMPLES</span></span>

### <span data-ttu-id="db2c6-115">예제 1 - AD 서비스 주체 나열</span><span class="sxs-lookup"><span data-stu-id="db2c6-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="db2c6-116">테넌트의 모든 AD 서비스 주체가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="db2c6-117">예제 2 - Paging를 사용하여 AD 서비스 주체 나열</span><span class="sxs-lookup"><span data-stu-id="db2c6-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="db2c6-118">테넌트에 처음 100개 AD 서비스 주체가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="db2c6-119">예제 3 - SPN으로 서비스 주체 나열</span><span class="sxs-lookup"><span data-stu-id="db2c6-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="db2c6-120">SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'가 있는 서비스 주체 나열</span><span class="sxs-lookup"><span data-stu-id="db2c6-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="db2c6-121">예제 4 - 검색 문자열로 서비스 주체 나열</span><span class="sxs-lookup"><span data-stu-id="db2c6-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="db2c6-122">표시 이름이 "웹"으로 시작하는 모든 AD 서비스 주체가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="db2c6-123">예제 5 - 파이핑을 통해 서비스 주체 나열</span><span class="sxs-lookup"><span data-stu-id="db2c6-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="db2c6-124">개체 ID가 '39e64ec6-569b-4030-8e1c-c3c519a05d69'인 AD 애플리케이션을 시작하고 Get-AzADServicePrincipal cmdlet에 파이프하여 해당 애플리케이션의 모든 서비스 주체 목록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="db2c6-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db2c6-125">PARAMETERS</span></span>

### <span data-ttu-id="db2c6-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="db2c6-126">-ApplicationId</span></span>
<span data-ttu-id="db2c6-127">서비스 주체 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-127">The service principal application id.</span></span>

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

### <span data-ttu-id="db2c6-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="db2c6-128">-ApplicationObject</span></span>
<span data-ttu-id="db2c6-129">서비스 주체가 검색되는 애플리케이션 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db2c6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db2c6-130">-DefaultProfile</span></span>
<span data-ttu-id="db2c6-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="db2c6-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db2c6-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db2c6-132">-DisplayName</span></span>
<span data-ttu-id="db2c6-133">서비스 주체 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-133">The service principal display name.</span></span>

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

### <span data-ttu-id="db2c6-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="db2c6-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="db2c6-135">서비스 주체 검색 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-135">The service principal search string.</span></span>

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

### <span data-ttu-id="db2c6-136">-First</span><span class="sxs-lookup"><span data-stu-id="db2c6-136">-First</span></span>
<span data-ttu-id="db2c6-137">반환할 개체의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="db2c6-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="db2c6-138">-IncludeTotalCount</span></span>
<span data-ttu-id="db2c6-139">데이터 집합의 개체 수를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="db2c6-140">현재 이 매개 변수는 아무 것도 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="db2c6-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="db2c6-141">-ObjectId</span></span>
<span data-ttu-id="db2c6-142">서비스 주체의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-142">Object id of the service principal.</span></span>

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

### <span data-ttu-id="db2c6-143">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="db2c6-143">-ServicePrincipalName</span></span>
<span data-ttu-id="db2c6-144">서비스의 SPN입니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-144">SPN of the service.</span></span>

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

### <span data-ttu-id="db2c6-145">-Skip</span><span class="sxs-lookup"><span data-stu-id="db2c6-145">-Skip</span></span>
<span data-ttu-id="db2c6-146">첫 번째 N개 개체를 무시하고 나머지 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="db2c6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2c6-147">CommonParameters</span></span>
<span data-ttu-id="db2c6-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="db2c6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db2c6-149">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="db2c6-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2c6-150">입력</span><span class="sxs-lookup"><span data-stu-id="db2c6-150">INPUTS</span></span>

### <span data-ttu-id="db2c6-151">System.String</span><span class="sxs-lookup"><span data-stu-id="db2c6-151">System.String</span></span>

### <span data-ttu-id="db2c6-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="db2c6-152">System.Guid</span></span>

### <span data-ttu-id="db2c6-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="db2c6-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="db2c6-154">매개 변수: ApplicationObject(ByValue)</span><span class="sxs-lookup"><span data-stu-id="db2c6-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="db2c6-155">출력</span><span class="sxs-lookup"><span data-stu-id="db2c6-155">OUTPUTS</span></span>

### <span data-ttu-id="db2c6-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="db2c6-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="db2c6-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="db2c6-157">NOTES</span></span>

## <span data-ttu-id="db2c6-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db2c6-158">RELATED LINKS</span></span>

[<span data-ttu-id="db2c6-159">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="db2c6-159">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)


[<span data-ttu-id="db2c6-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="db2c6-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="db2c6-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="db2c6-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="db2c6-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="db2c6-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

