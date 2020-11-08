---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 4a4888573199c4fd5f76282fb5c8eb1702911e00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047645"
---
# <span data-ttu-id="c539d-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c539d-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="c539d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c539d-102">SYNOPSIS</span></span>
<span data-ttu-id="c539d-103">기존 azure active directory 서비스 주체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="c539d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c539d-104">SYNTAX</span></span>

### <span data-ttu-id="c539d-105">SpObjectIdWithDisplayNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c539d-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c539d-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c539d-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c539d-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c539d-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c539d-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c539d-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c539d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c539d-109">DESCRIPTION</span></span>
<span data-ttu-id="c539d-110">기존 azure active directory 서비스 주체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="c539d-111">이 서비스 사용자와 연결 된 자격 증명을 업데이트 하려면 New-AzADSpCredential cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="c539d-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="c539d-112">기본 응용 프로그램과 연결 된 속성을 업데이트 하려면 Update-AzADApplication cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="c539d-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="c539d-113">예제의</span><span class="sxs-lookup"><span data-stu-id="c539d-113">EXAMPLES</span></span>

### <span data-ttu-id="c539d-114">예제 1: 서비스 주체의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="c539d-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="c539d-115">개체 id가 ' 784136ca-3ae2-4fdd-a388-89d793e7c780 ' 인 서비스 주체의 표시 이름을 ' MyNewDisplayName '로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="c539d-116">예제 2: 파이핑을 사용 하 여 서비스 주체의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="c539d-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="c539d-117">개체 id가 ' 784136ca-3ae2-4fdd-a388-89d793e7c780 ' 인 서비스 사용자를 가져오고 서비스 사용자의 표시 이름을 "MyNewDisplayName"로 업데이트 하도록 Update-AzADServicePrincipal cmdlet에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="c539d-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="c539d-118">Example 3</span></span>

<span data-ttu-id="c539d-119">기존 azure active directory 서비스 주체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="c539d-120">생성</span><span class="sxs-lookup"><span data-stu-id="c539d-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="c539d-121">변수</span><span class="sxs-lookup"><span data-stu-id="c539d-121">PARAMETERS</span></span>

### <span data-ttu-id="c539d-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c539d-122">-ApplicationId</span></span>
<span data-ttu-id="c539d-123">업데이트할 서비스 주체의 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-123">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="c539d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c539d-124">-DefaultProfile</span></span>
<span data-ttu-id="c539d-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c539d-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c539d-126">-DisplayName</span></span>
<span data-ttu-id="c539d-127">서비스 주체의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-127">The display name for the service principal.</span></span>

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

### <span data-ttu-id="c539d-128">-홈페이지</span><span class="sxs-lookup"><span data-stu-id="c539d-128">-Homepage</span></span>
<span data-ttu-id="c539d-129">서비스 사용자의 홈페이지입니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-129">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="c539d-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="c539d-130">-IdentifierUri</span></span>
<span data-ttu-id="c539d-131">서비스 사용자의 식별자 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-131">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="c539d-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c539d-132">-InputObject</span></span>
<span data-ttu-id="c539d-133">업데이트할 서비스 사용자를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-133">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="c539d-134">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="c539d-134">-KeyCredential</span></span>
<span data-ttu-id="c539d-135">서비스 사용자의 키 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-135">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="c539d-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c539d-136">-ObjectId</span></span>
<span data-ttu-id="c539d-137">업데이트할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-137">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="c539d-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="c539d-138">-PasswordCredential</span></span>
<span data-ttu-id="c539d-139">서비스 사용자의 암호 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-139">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="c539d-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c539d-140">-ServicePrincipalName</span></span>
<span data-ttu-id="c539d-141">업데이트할 서비스 주체의 SPN입니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-141">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="c539d-142">-확인</span><span class="sxs-lookup"><span data-stu-id="c539d-142">-Confirm</span></span>
<span data-ttu-id="c539d-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c539d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c539d-144">-WhatIf</span></span>
<span data-ttu-id="c539d-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c539d-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c539d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c539d-147">CommonParameters</span></span>
<span data-ttu-id="c539d-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c539d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c539d-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c539d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c539d-150">입력</span><span class="sxs-lookup"><span data-stu-id="c539d-150">INPUTS</span></span>

### <span data-ttu-id="c539d-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c539d-151">System.String</span></span>

### <span data-ttu-id="c539d-152">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="c539d-152">System.Guid</span></span>

### <span data-ttu-id="c539d-153">ActiveDirectory PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c539d-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c539d-154">출력</span><span class="sxs-lookup"><span data-stu-id="c539d-154">OUTPUTS</span></span>

### <span data-ttu-id="c539d-155">ActiveDirectory PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c539d-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c539d-156">상속자</span><span class="sxs-lookup"><span data-stu-id="c539d-156">NOTES</span></span>

## <span data-ttu-id="c539d-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c539d-157">RELATED LINKS</span></span>
