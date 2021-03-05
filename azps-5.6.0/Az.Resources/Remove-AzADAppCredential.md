---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 93e2b62cf1261b20df1ea6c90d48caa1e1d88ec2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982192"
---
# <span data-ttu-id="5a795-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5a795-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="5a795-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a795-102">SYNOPSIS</span></span>
<span data-ttu-id="5a795-103">애플리케이션에서 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="5a795-104">구문</span><span class="sxs-lookup"><span data-stu-id="5a795-104">SYNTAX</span></span>

### <span data-ttu-id="5a795-105">ApplicationObjectIdWithKeyIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5a795-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a795-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a795-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a795-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a795-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a795-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a795-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a795-109">설명</span><span class="sxs-lookup"><span data-stu-id="5a795-109">DESCRIPTION</span></span>
<span data-ttu-id="5a795-110">Remove-AzADAppCredential cmdlet은 손상된 경우 또는 자격 증명 키 롤오버 만료의 일부로 애플리케이션에서 자격 증명 키를 제거하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="5a795-111">애플리케이션은 개체 ID 또는 AppId를 제공하여 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="5a795-112">제거할 자격 증명은 키 ID로 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="5a795-113">예제</span><span class="sxs-lookup"><span data-stu-id="5a795-113">EXAMPLES</span></span>

### <span data-ttu-id="5a795-114">예제 1: 애플리케이션에서 특정 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="5a795-114">Example 1: Remove a specific credential from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="5a795-115">개체 ID '7663d3fb-6f86-4352-9e6d50d-cf9d50d5ee82'를 사용하여 애플리케이션에서 키 ID '904423-60a3-45a3-450d5ee82'로 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="5a795-116">예제 2: 애플리케이션에서 모든 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="5a795-116">Example 2: Remove all credentials from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="5a795-117">애플리케이션 ID '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'을 사용하여 애플리케이션에서 모든 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="5a795-118">예제 3: 배관을 사용하여 모든 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="5a795-118">Example 3: Remove all credentials using piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="5a795-119">개체 ID '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'를 사용하여 애플리케이션을 Remove-AzADAppCredential cmdlet에 연결하고 해당 애플리케이션에서 모든 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="5a795-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5a795-120">PARAMETERS</span></span>

### <span data-ttu-id="5a795-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5a795-121">-ApplicationId</span></span>
<span data-ttu-id="5a795-122">자격 증명을 제거할 애플리케이션의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="5a795-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="5a795-123">-ApplicationObject</span></span>
<span data-ttu-id="5a795-124">자격 증명을 제거하는 애플리케이션 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-124">The application object to remove the credentials from.</span></span>

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

### <span data-ttu-id="5a795-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a795-125">-DefaultProfile</span></span>
<span data-ttu-id="5a795-126">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5a795-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a795-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5a795-127">-DisplayName</span></span>
<span data-ttu-id="5a795-128">애플리케이션의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-128">The display name of the application.</span></span>

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

### <span data-ttu-id="5a795-129">-Force</span><span class="sxs-lookup"><span data-stu-id="5a795-129">-Force</span></span>
<span data-ttu-id="5a795-130">확인 없이 자격 증명을 삭제로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="5a795-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="5a795-131">-KeyId</span></span>
<span data-ttu-id="5a795-132">제거할 자격 증명 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="5a795-133">애플리케이션에 대한 키 ID는 cmdlet을 사용하여 Get-AzADAppCredential 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="5a795-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5a795-134">-ObjectId</span></span>
<span data-ttu-id="5a795-135">자격 증명을 제거하는 애플리케이션의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-135">The object id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="5a795-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a795-136">-PassThru</span></span>
<span data-ttu-id="5a795-137">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5a795-138">-확인</span><span class="sxs-lookup"><span data-stu-id="5a795-138">-Confirm</span></span>
<span data-ttu-id="5a795-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a795-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a795-140">-WhatIf</span></span>
<span data-ttu-id="5a795-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a795-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a795-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a795-143">CommonParameters</span></span>
<span data-ttu-id="5a795-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5a795-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a795-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a795-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a795-146">입력</span><span class="sxs-lookup"><span data-stu-id="5a795-146">INPUTS</span></span>

### <span data-ttu-id="5a795-147">System.String</span><span class="sxs-lookup"><span data-stu-id="5a795-147">System.String</span></span>

### <span data-ttu-id="5a795-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5a795-148">System.Guid</span></span>

### <span data-ttu-id="5a795-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="5a795-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="5a795-150">출력</span><span class="sxs-lookup"><span data-stu-id="5a795-150">OUTPUTS</span></span>

### <span data-ttu-id="5a795-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a795-151">System.Boolean</span></span>

## <span data-ttu-id="5a795-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5a795-152">NOTES</span></span>

## <span data-ttu-id="5a795-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a795-153">RELATED LINKS</span></span>

[<span data-ttu-id="5a795-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5a795-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="5a795-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5a795-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="5a795-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="5a795-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
