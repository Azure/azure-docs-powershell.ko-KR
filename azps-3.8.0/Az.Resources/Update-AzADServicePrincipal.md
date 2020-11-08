---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 19d8c4e3a47f7b75073d0207d000b8f18a5c0f6f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041695"
---
# <span data-ttu-id="21cb1-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="21cb1-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="21cb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="21cb1-103">기존 azure active directory 서비스 주체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="21cb1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="21cb1-104">SYNTAX</span></span>

### <span data-ttu-id="21cb1-105">SpObjectIdWithDisplayNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="21cb1-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21cb1-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="21cb1-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21cb1-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="21cb1-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21cb1-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="21cb1-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21cb1-109">설명은</span><span class="sxs-lookup"><span data-stu-id="21cb1-109">DESCRIPTION</span></span>
<span data-ttu-id="21cb1-110">기존 azure active directory 서비스 주체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="21cb1-111">이 서비스 사용자와 연결 된 자격 증명을 업데이트 하려면 New-AzADSpCredential cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="21cb1-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="21cb1-112">기본 응용 프로그램과 연결 된 속성을 업데이트 하려면 Update-AzADApplication cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="21cb1-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="21cb1-113">예제의</span><span class="sxs-lookup"><span data-stu-id="21cb1-113">EXAMPLES</span></span>

### <span data-ttu-id="21cb1-114">예제 1-서비스 주체의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="21cb1-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="21cb1-115">개체 id가 ' 784136ca-3ae2-4fdd-a388-89d793e7c780 ' 인 서비스 주체의 표시 이름을 ' MyNewDisplayName '로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="21cb1-116">예제 2-파이핑을 사용 하 여 서비스 주체의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="21cb1-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="21cb1-117">개체 id가 ' 784136ca-3ae2-4fdd-a388-89d793e7c780 ' 인 서비스 사용자를 가져오고 서비스 사용자의 표시 이름을 "MyNewDisplayName"로 업데이트 하도록 Update-AzADServicePrincipal cmdlet에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="21cb1-118">변수</span><span class="sxs-lookup"><span data-stu-id="21cb1-118">PARAMETERS</span></span>

### <span data-ttu-id="21cb1-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="21cb1-119">-ApplicationId</span></span>
<span data-ttu-id="21cb1-120">업데이트할 서비스 주체의 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="21cb1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21cb1-121">-DefaultProfile</span></span>
<span data-ttu-id="21cb1-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21cb1-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="21cb1-123">-DisplayName</span></span>
<span data-ttu-id="21cb1-124">서비스 주체의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="21cb1-125">-홈페이지</span><span class="sxs-lookup"><span data-stu-id="21cb1-125">-Homepage</span></span>
<span data-ttu-id="21cb1-126">서비스 사용자의 홈페이지입니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="21cb1-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="21cb1-127">-IdentifierUri</span></span>
<span data-ttu-id="21cb1-128">서비스 사용자의 식별자 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="21cb1-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21cb1-129">-InputObject</span></span>
<span data-ttu-id="21cb1-130">업데이트할 서비스 사용자를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-130">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="21cb1-131">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="21cb1-131">-KeyCredential</span></span>
<span data-ttu-id="21cb1-132">서비스 사용자의 키 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-132">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="21cb1-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="21cb1-133">-ObjectId</span></span>
<span data-ttu-id="21cb1-134">업데이트할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-134">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="21cb1-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="21cb1-135">-PasswordCredential</span></span>
<span data-ttu-id="21cb1-136">서비스 사용자의 암호 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-136">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="21cb1-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="21cb1-137">-ServicePrincipalName</span></span>
<span data-ttu-id="21cb1-138">업데이트할 서비스 주체의 SPN입니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="21cb1-139">-확인</span><span class="sxs-lookup"><span data-stu-id="21cb1-139">-Confirm</span></span>
<span data-ttu-id="21cb1-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21cb1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21cb1-141">-WhatIf</span></span>
<span data-ttu-id="21cb1-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21cb1-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21cb1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21cb1-144">CommonParameters</span></span>
<span data-ttu-id="21cb1-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="21cb1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21cb1-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="21cb1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21cb1-147">입력</span><span class="sxs-lookup"><span data-stu-id="21cb1-147">INPUTS</span></span>

### <span data-ttu-id="21cb1-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="21cb1-148">System.String</span></span>

### <span data-ttu-id="21cb1-149">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="21cb1-149">System.Guid</span></span>

### <span data-ttu-id="21cb1-150">ActiveDirectory PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="21cb1-150">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="21cb1-151">출력</span><span class="sxs-lookup"><span data-stu-id="21cb1-151">OUTPUTS</span></span>

### <span data-ttu-id="21cb1-152">ActiveDirectory PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="21cb1-152">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="21cb1-153">상속자</span><span class="sxs-lookup"><span data-stu-id="21cb1-153">NOTES</span></span>

## <span data-ttu-id="21cb1-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21cb1-154">RELATED LINKS</span></span>
