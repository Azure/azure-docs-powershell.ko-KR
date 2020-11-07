---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: d40c1a3a5e626d364986352f95bc914b31ced969
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699354"
---
# <span data-ttu-id="34261-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="34261-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="34261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34261-102">SYNOPSIS</span></span>
<span data-ttu-id="34261-103">서비스 사용자에서 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="34261-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="34261-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34261-104">SYNTAX</span></span>

### <span data-ttu-id="34261-105">ObjectIdWithKeyIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="34261-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34261-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34261-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34261-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34261-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34261-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34261-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34261-109">설명은</span><span class="sxs-lookup"><span data-stu-id="34261-109">DESCRIPTION</span></span>
<span data-ttu-id="34261-110">Remove-AzADSpCredential cmdlet을 사용 하 여 손상 되거나 자격 증명 키 롤오버 만료의 일부인 경우 서비스 사용자가 자격 증명 키를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34261-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="34261-111">서비스 사용자는 개체 ID 또는 SPN (서비스 사용자 이름) 중 하나를 제공 하 여 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34261-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="34261-112">제거할 자격 증명은 개별 자격 증명을 제거 하거나 ' 모두 ' 스위치를 사용 하 여 서비스 사용자와 연결 된 모든 자격 증명을 삭제 하는 경우 해당 키 ID로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34261-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="34261-113">예제의</span><span class="sxs-lookup"><span data-stu-id="34261-113">EXAMPLES</span></span>

### <span data-ttu-id="34261-114">예제 1-서비스 사용자에서 특정 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="34261-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="34261-115">개체 id가 ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' 인 서비스 사용자의 키 id가 9044423a-60a3-45ac-9ab1-09534157ebb ' 인 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="34261-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="34261-116">예제 2-서비스 사용자의 모든 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="34261-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="34261-117">SPN이 "" 인 서비스 사용자의 모든 자격 증명을 제거 http://test123 합니다.</span><span class="sxs-lookup"><span data-stu-id="34261-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="34261-118">예제 3-파이핑을 사용 하 여 서비스 사용자의 모든 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="34261-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="34261-119">개체 id가 ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' 인 서비스 사용자를 가져오고 해당 서비스 사용자의 모든 자격 증명을 제거 하도록 Remove-AzADSpCredential cmdlet에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="34261-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="34261-120">변수</span><span class="sxs-lookup"><span data-stu-id="34261-120">PARAMETERS</span></span>

### <span data-ttu-id="34261-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34261-121">-DefaultProfile</span></span>
<span data-ttu-id="34261-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="34261-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34261-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="34261-123">-DisplayName</span></span>
<span data-ttu-id="34261-124">서비스 주체의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34261-124">The display name of the service principal.</span></span>

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

### <span data-ttu-id="34261-125">-Force</span><span class="sxs-lookup"><span data-stu-id="34261-125">-Force</span></span>
<span data-ttu-id="34261-126">확인 하지 않고 자격 증명 삭제로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="34261-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="34261-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="34261-127">-KeyId</span></span>
<span data-ttu-id="34261-128">제거할 자격 증명 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34261-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="34261-129">서비스 사용자의 키 Id는 Get-AzADSpCredential cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34261-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

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

### <span data-ttu-id="34261-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="34261-130">-ObjectId</span></span>
<span data-ttu-id="34261-131">자격 증명을 제거할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="34261-131">The object id of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="34261-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34261-132">-PassThru</span></span>
<span data-ttu-id="34261-133">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="34261-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="34261-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="34261-134">-ServicePrincipalName</span></span>
<span data-ttu-id="34261-135">자격 증명을 제거할 서비스 주체의 이름 (SPN)입니다.</span><span class="sxs-lookup"><span data-stu-id="34261-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="34261-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="34261-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="34261-137">자격 증명을 제거할 서비스 사용자 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="34261-137">The service principal object to remove the credentials from.</span></span>

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

### <span data-ttu-id="34261-138">-확인</span><span class="sxs-lookup"><span data-stu-id="34261-138">-Confirm</span></span>
<span data-ttu-id="34261-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="34261-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34261-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34261-140">-WhatIf</span></span>
<span data-ttu-id="34261-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="34261-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34261-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34261-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34261-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34261-143">CommonParameters</span></span>
<span data-ttu-id="34261-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34261-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34261-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34261-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34261-146">입력</span><span class="sxs-lookup"><span data-stu-id="34261-146">INPUTS</span></span>

### <span data-ttu-id="34261-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="34261-147">System.String</span></span>

### <span data-ttu-id="34261-148">ActiveDirectory PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="34261-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="34261-149">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="34261-149">System.Guid</span></span>

## <span data-ttu-id="34261-150">출력</span><span class="sxs-lookup"><span data-stu-id="34261-150">OUTPUTS</span></span>

### <span data-ttu-id="34261-151">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="34261-151">System.Boolean</span></span>

## <span data-ttu-id="34261-152">상속자</span><span class="sxs-lookup"><span data-stu-id="34261-152">NOTES</span></span>

## <span data-ttu-id="34261-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34261-153">RELATED LINKS</span></span>

[<span data-ttu-id="34261-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="34261-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="34261-155">새로운 AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="34261-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="34261-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="34261-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)
