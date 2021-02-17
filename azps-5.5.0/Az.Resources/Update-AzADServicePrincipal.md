---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 05bd5f7997c83c2be6b50faf0e6d88ee7413a773
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183617"
---
# <span data-ttu-id="c14dd-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c14dd-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="c14dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c14dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c14dd-103">기존 Azure Active Directory 서비스 주체 업데이트</span><span class="sxs-lookup"><span data-stu-id="c14dd-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="c14dd-104">구문</span><span class="sxs-lookup"><span data-stu-id="c14dd-104">SYNTAX</span></span>

### <span data-ttu-id="c14dd-105">SpObjectIdWithDisplayNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c14dd-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14dd-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c14dd-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14dd-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c14dd-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14dd-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c14dd-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c14dd-109">설명</span><span class="sxs-lookup"><span data-stu-id="c14dd-109">DESCRIPTION</span></span>
<span data-ttu-id="c14dd-110">기존 Azure Active Directory 서비스 주체 업데이트</span><span class="sxs-lookup"><span data-stu-id="c14dd-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="c14dd-111">이 서비스 주체와 연결된 자격 증명을 업데이트하기 위해 New-AzADSpCredential cmdlet을 사용하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="c14dd-112">기본 애플리케이션과 연결된 속성을 업데이트하기 위해 Update-AzADApplication cmdlet을 사용하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="c14dd-113">예제</span><span class="sxs-lookup"><span data-stu-id="c14dd-113">EXAMPLES</span></span>

### <span data-ttu-id="c14dd-114">예제 1: 서비스 주체의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="c14dd-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="c14dd-115">개체 ID '784136ca-3ae2-4fdd-a388-89d793e7c780'을 'MyNewDisplayName'으로 서비스 주체의 표시 이름을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="c14dd-116">예제 2: 파이핑을 사용하여 서비스 주체의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="c14dd-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="c14dd-117">개체 ID가 '784136ca-3ae2-4fdd-a388-89d793e7c780'인 서비스 주체와 서비스 주체의 표시 이름을 "MyNewDisplayName"으로 업데이트하기 위해 Update-AzADServicePrincipal cmdlet에 파이프합니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="c14dd-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="c14dd-118">Example 3</span></span>

<span data-ttu-id="c14dd-119">기존 Azure Active Directory 서비스 주체 업데이트</span><span class="sxs-lookup"><span data-stu-id="c14dd-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="c14dd-120">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="c14dd-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="c14dd-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c14dd-121">PARAMETERS</span></span>

### <span data-ttu-id="c14dd-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c14dd-122">-ApplicationId</span></span>
<span data-ttu-id="c14dd-123">업데이트할 서비스 주체의 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-123">The application id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpApplicationIdWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c14dd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14dd-124">-DefaultProfile</span></span>
<span data-ttu-id="c14dd-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c14dd-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c14dd-126">-DisplayName</span></span>
<span data-ttu-id="c14dd-127">서비스 주체의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-127">The display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet, SPNWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c14dd-128">-Homepage</span><span class="sxs-lookup"><span data-stu-id="c14dd-128">-Homepage</span></span>
<span data-ttu-id="c14dd-129">서비스 주체에 대한 홈페이지입니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-129">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="c14dd-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="c14dd-130">-IdentifierUri</span></span>
<span data-ttu-id="c14dd-131">서비스 주체에 대한 식별자 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-131">The identifier URI(s) for the service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14dd-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c14dd-132">-InputObject</span></span>
<span data-ttu-id="c14dd-133">업데이트할 서비스 주체를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-133">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c14dd-134">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="c14dd-134">-KeyCredential</span></span>
<span data-ttu-id="c14dd-135">서비스 주체에 대한 키 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-135">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14dd-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c14dd-136">-ObjectId</span></span>
<span data-ttu-id="c14dd-137">업데이트할 서비스 주체의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-137">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c14dd-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="c14dd-138">-PasswordCredential</span></span>
<span data-ttu-id="c14dd-139">서비스 주체에 대한 암호 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-139">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14dd-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c14dd-140">-ServicePrincipalName</span></span>
<span data-ttu-id="c14dd-141">업데이트할 서비스 주체의 SPN입니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-141">The SPN of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c14dd-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c14dd-142">-Confirm</span></span>
<span data-ttu-id="c14dd-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c14dd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c14dd-144">-WhatIf</span></span>
<span data-ttu-id="c14dd-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c14dd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c14dd-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c14dd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14dd-147">CommonParameters</span></span>
<span data-ttu-id="c14dd-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c14dd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14dd-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c14dd-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14dd-150">입력</span><span class="sxs-lookup"><span data-stu-id="c14dd-150">INPUTS</span></span>

### <span data-ttu-id="c14dd-151">System.String</span><span class="sxs-lookup"><span data-stu-id="c14dd-151">System.String</span></span>

### <span data-ttu-id="c14dd-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c14dd-152">System.Guid</span></span>

### <span data-ttu-id="c14dd-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c14dd-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c14dd-154">출력</span><span class="sxs-lookup"><span data-stu-id="c14dd-154">OUTPUTS</span></span>

### <span data-ttu-id="c14dd-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c14dd-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c14dd-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c14dd-156">NOTES</span></span>

## <span data-ttu-id="c14dd-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c14dd-157">RELATED LINKS</span></span>