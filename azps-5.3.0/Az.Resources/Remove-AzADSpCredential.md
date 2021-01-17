---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: bcb33f87b85eb6ad5bce9ba812ebccb4d154e920
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490316"
---
# <span data-ttu-id="6c8e2-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6c8e2-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="6c8e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c8e2-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8e2-103">서비스 주체에서 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="6c8e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="6c8e2-104">SYNTAX</span></span>

### <span data-ttu-id="6c8e2-105">ObjectIdWithKeyIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6c8e2-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c8e2-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c8e2-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c8e2-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c8e2-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c8e2-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c8e2-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c8e2-109">설명</span><span class="sxs-lookup"><span data-stu-id="6c8e2-109">DESCRIPTION</span></span>
<span data-ttu-id="6c8e2-110">이 Remove-AzADSpCredential cmdlet을 사용하여 손상된 경우 또는 자격 증명 키 롤오버 만료의 일부로 서비스 주체에서 자격 증명 키를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="6c8e2-111">서비스 주체는 개체 ID 또는 SPN(서비스 주체 이름)을 제공하여 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="6c8e2-112">개별 자격 증명을 제거하거나 '모두' 스위치를 사용하여 서비스 주체와 연결된 모든 자격 증명을 삭제하는 경우 제거할 자격 증명은 키 ID로 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="6c8e2-113">예제</span><span class="sxs-lookup"><span data-stu-id="6c8e2-113">EXAMPLES</span></span>

### <span data-ttu-id="6c8e2-114">예제 1: 서비스 주체에서 특정 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="6c8e2-114">Example 1: Remove a specific credential from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="6c8e2-115">개체 ID가 '7663d3fb-6f86-4352-9e6d50d5ee82'인 서비스 주체에서 키 ID가 '9044423a-60a3-45ac-9ab1-09534157ebb'인 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="6c8e2-116">예제 2: 서비스 주체에서 모든 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="6c8e2-116">Example 2: Remove all credentials from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="6c8e2-117">SPN " "를 사용하여 서비스 주체에서 모든 자격 증명을 http://test123 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="6c8e2-118">예제 3: 파이핑을 사용하여 서비스 주체에서 모든 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="6c8e2-118">Example 3: Remove all credentials from a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="6c8e2-119">개체 ID가 '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'인 서비스 주체 및 Remove-AzADSpCredential cmdlet에 파이프하여 해당 서비스 주체에서 모든 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="6c8e2-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c8e2-120">PARAMETERS</span></span>

### <span data-ttu-id="6c8e2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c8e2-121">-DefaultProfile</span></span>
<span data-ttu-id="6c8e2-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6c8e2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c8e2-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6c8e2-123">-DisplayName</span></span>
<span data-ttu-id="6c8e2-124">서비스 주체의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-124">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8e2-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6c8e2-125">-Force</span></span>
<span data-ttu-id="6c8e2-126">확인 없이 자격 증명을 삭제하려면 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="6c8e2-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="6c8e2-127">-KeyId</span></span>
<span data-ttu-id="6c8e2-128">제거할 자격 증명 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="6c8e2-129">서비스 주체에 대한 키 ID는 Get-AzADSpCredential 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8e2-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6c8e2-130">-ObjectId</span></span>
<span data-ttu-id="6c8e2-131">자격 증명을 제거할 서비스 주체의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8e2-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c8e2-132">-PassThru</span></span>
<span data-ttu-id="6c8e2-133">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6c8e2-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="6c8e2-134">-ServicePrincipalName</span></span>
<span data-ttu-id="6c8e2-135">자격 증명을 제거할 서비스 주체의 SPN(이름)입니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8e2-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="6c8e2-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="6c8e2-137">자격 증명을 제거할 서비스 주체 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8e2-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c8e2-138">-Confirm</span></span>
<span data-ttu-id="6c8e2-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c8e2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c8e2-140">-WhatIf</span></span>
<span data-ttu-id="6c8e2-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6c8e2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c8e2-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c8e2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8e2-143">CommonParameters</span></span>
<span data-ttu-id="6c8e2-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c8e2-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c8e2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8e2-146">입력</span><span class="sxs-lookup"><span data-stu-id="6c8e2-146">INPUTS</span></span>

### <span data-ttu-id="6c8e2-147">System.String</span><span class="sxs-lookup"><span data-stu-id="6c8e2-147">System.String</span></span>

### <span data-ttu-id="6c8e2-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6c8e2-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="6c8e2-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="6c8e2-149">System.Guid</span></span>

## <span data-ttu-id="6c8e2-150">출력</span><span class="sxs-lookup"><span data-stu-id="6c8e2-150">OUTPUTS</span></span>

### <span data-ttu-id="6c8e2-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c8e2-151">System.Boolean</span></span>

## <span data-ttu-id="6c8e2-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6c8e2-152">NOTES</span></span>

## <span data-ttu-id="6c8e2-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c8e2-153">RELATED LINKS</span></span>

[<span data-ttu-id="6c8e2-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6c8e2-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="6c8e2-155">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6c8e2-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="6c8e2-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6c8e2-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

