---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: f6344590828663a0cf44d96d6fe733adff8757c5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362909"
---
# <span data-ttu-id="090d1-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="090d1-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="090d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="090d1-102">SYNOPSIS</span></span>
<span data-ttu-id="090d1-103">애플리케이션에서 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="090d1-104">구문</span><span class="sxs-lookup"><span data-stu-id="090d1-104">SYNTAX</span></span>

### <span data-ttu-id="090d1-105">ApplicationObjectIdWithKeyIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="090d1-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="090d1-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="090d1-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="090d1-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="090d1-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="090d1-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="090d1-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="090d1-109">설명</span><span class="sxs-lookup"><span data-stu-id="090d1-109">DESCRIPTION</span></span>
<span data-ttu-id="090d1-110">이 Remove-AzADAppCredential cmdlet을 사용하여 손상된 경우 또는 자격 증명 키 롤오버 만료의 일부로 애플리케이션에서 자격 증명 키를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="090d1-111">애플리케이션은 개체 ID 또는 AppId를 제공하여 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="090d1-112">제거할 자격 증명은 키 ID로 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="090d1-113">예제</span><span class="sxs-lookup"><span data-stu-id="090d1-113">EXAMPLES</span></span>

### <span data-ttu-id="090d1-114">예제 1: 애플리케이션에서 특정 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="090d1-114">Example 1: Remove a specific credential from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="090d1-115">개체 ID가 '7663d3fb-6f86-4352-9e6d50d5ee82'인 애플리케이션에서 키 ID가 '9044423a-60a3-45ac-9ab1-09534157ebb'인 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="090d1-116">예제 2: 애플리케이션에서 모든 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="090d1-116">Example 2: Remove all credentials from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="090d1-117">애플리케이션 ID가 '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'인 애플리케이션에서 모든 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="090d1-118">예제 3: 파이핑을 사용하여 모든 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="090d1-118">Example 3: Remove all credentials using piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="090d1-119">개체 ID가 '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'인 애플리케이션을 Remove-AzADAppCredential cmdlet에 파이프하고 해당 애플리케이션에서 모든 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="090d1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="090d1-120">PARAMETERS</span></span>

### <span data-ttu-id="090d1-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="090d1-121">-ApplicationId</span></span>
<span data-ttu-id="090d1-122">자격 증명을 제거할 애플리케이션의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="090d1-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="090d1-123">-ApplicationObject</span></span>
<span data-ttu-id="090d1-124">자격 증명을 제거할 애플리케이션 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="090d1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="090d1-125">-DefaultProfile</span></span>
<span data-ttu-id="090d1-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="090d1-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="090d1-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="090d1-127">-DisplayName</span></span>
<span data-ttu-id="090d1-128">애플리케이션의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-128">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="090d1-129">-Force</span><span class="sxs-lookup"><span data-stu-id="090d1-129">-Force</span></span>
<span data-ttu-id="090d1-130">확인 없이 자격 증명을 삭제하려면 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="090d1-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="090d1-131">-KeyId</span></span>
<span data-ttu-id="090d1-132">제거할 자격 증명 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="090d1-133">애플리케이션에 대한 키 ID는 Get-AzADAppCredential 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="090d1-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="090d1-134">-ObjectId</span></span>
<span data-ttu-id="090d1-135">자격 증명을 제거할 애플리케이션의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="090d1-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="090d1-136">-PassThru</span></span>
<span data-ttu-id="090d1-137">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="090d1-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="090d1-138">-Confirm</span></span>
<span data-ttu-id="090d1-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="090d1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="090d1-140">-WhatIf</span></span>
<span data-ttu-id="090d1-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="090d1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="090d1-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="090d1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="090d1-143">CommonParameters</span></span>
<span data-ttu-id="090d1-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="090d1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="090d1-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="090d1-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="090d1-146">입력</span><span class="sxs-lookup"><span data-stu-id="090d1-146">INPUTS</span></span>

### <span data-ttu-id="090d1-147">System.String</span><span class="sxs-lookup"><span data-stu-id="090d1-147">System.String</span></span>

### <span data-ttu-id="090d1-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="090d1-148">System.Guid</span></span>

### <span data-ttu-id="090d1-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="090d1-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="090d1-150">출력</span><span class="sxs-lookup"><span data-stu-id="090d1-150">OUTPUTS</span></span>

### <span data-ttu-id="090d1-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="090d1-151">System.Boolean</span></span>

## <span data-ttu-id="090d1-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="090d1-152">NOTES</span></span>

## <span data-ttu-id="090d1-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="090d1-153">RELATED LINKS</span></span>

[<span data-ttu-id="090d1-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="090d1-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="090d1-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="090d1-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="090d1-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="090d1-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
