---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: c4754ecf8cae06fd43f57bc50d3b3fbeaf1d5081
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347354"
---
# <span data-ttu-id="6adb4-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6adb4-101">Update-AzADApplication</span></span>

## <span data-ttu-id="6adb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6adb4-102">SYNOPSIS</span></span>
<span data-ttu-id="6adb4-103">기존 Azure Active Directory 애플리케이션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="6adb4-104">구문</span><span class="sxs-lookup"><span data-stu-id="6adb4-104">SYNTAX</span></span>

### <span data-ttu-id="6adb4-105">ApplicationObjectIdWithUpdateParamsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6adb4-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6adb4-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6adb4-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6adb4-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6adb4-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6adb4-108">설명</span><span class="sxs-lookup"><span data-stu-id="6adb4-108">DESCRIPTION</span></span>
<span data-ttu-id="6adb4-109">기존 Azure Active Directory 애플리케이션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="6adb4-110">이 애플리케이션과 연결된 자격 증명을 업데이트하기 위해 New-AzADAppCredential cmdlet을 사용하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="6adb4-111">예제</span><span class="sxs-lookup"><span data-stu-id="6adb4-111">EXAMPLES</span></span>

### <span data-ttu-id="6adb4-112">예제 1 - 애플리케이션의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="6adb4-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="6adb4-113">개체 ID 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'을 'MyNewDisplayName'으로 애플리케이션의 표시 이름을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="6adb4-114">예제 2 - 애플리케이션의 모든 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="6adb4-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="6adb4-115">개체 ID 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'로 애플리케이션의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="6adb4-116">예제 3 - 파이핑을 사용하여 애플리케이션의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="6adb4-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="6adb4-117">개체 ID가 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'인 애플리케이션을 다운로드하고 Update-AzADApplication cmdlet에 파이프하여 애플리케이션의 표시 이름을 "MyNewDisplayName"으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="6adb4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6adb4-118">PARAMETERS</span></span>

### <span data-ttu-id="6adb4-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6adb4-119">-ApplicationId</span></span>
<span data-ttu-id="6adb4-120">업데이트할 애플리케이션의 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-120">The application id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6adb4-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="6adb4-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="6adb4-122">애플리케이션이 다른 테넌트와 공유되는 경우 True입니다. 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-122">True if the application is shared with other tenants; otherwise, false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6adb4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6adb4-123">-DefaultProfile</span></span>
<span data-ttu-id="6adb4-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6adb4-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6adb4-125">-DisplayName</span></span>
<span data-ttu-id="6adb4-126">업데이트할 애플리케이션의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-126">The display name for the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6adb4-127">-HomePage</span><span class="sxs-lookup"><span data-stu-id="6adb4-127">-HomePage</span></span>
<span data-ttu-id="6adb4-128">애플리케이션의 홈페이지에 대한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-128">The URL to the application's homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6adb4-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="6adb4-129">-IdentifierUri</span></span>
<span data-ttu-id="6adb4-130">애플리케이션을 식별하는 UR입니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-130">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6adb4-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6adb4-131">-InputObject</span></span>
<span data-ttu-id="6adb4-132">업데이트할 애플리케이션을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6adb4-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6adb4-133">-ObjectId</span></span>
<span data-ttu-id="6adb4-134">업데이트할 애플리케이션의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-134">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6adb4-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="6adb4-135">-ReplyUrl</span></span>
<span data-ttu-id="6adb4-136">로그인을 위해 사용자 토큰이 전송된 URL 또는 OAuth 2.0 인증 코드 및 액세스 토큰이 전송된 리디렉션 URIS를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6adb4-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6adb4-137">-Confirm</span></span>
<span data-ttu-id="6adb4-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6adb4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6adb4-139">-WhatIf</span></span>
<span data-ttu-id="6adb4-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6adb4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6adb4-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6adb4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6adb4-142">CommonParameters</span></span>
<span data-ttu-id="6adb4-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6adb4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6adb4-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6adb4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6adb4-145">입력</span><span class="sxs-lookup"><span data-stu-id="6adb4-145">INPUTS</span></span>

### <span data-ttu-id="6adb4-146">System.String</span><span class="sxs-lookup"><span data-stu-id="6adb4-146">System.String</span></span>

### <span data-ttu-id="6adb4-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="6adb4-147">System.Guid</span></span>

### <span data-ttu-id="6adb4-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="6adb4-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="6adb4-149">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6adb4-149">System.String[]</span></span>

### <span data-ttu-id="6adb4-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6adb4-150">System.Boolean</span></span>

## <span data-ttu-id="6adb4-151">출력</span><span class="sxs-lookup"><span data-stu-id="6adb4-151">OUTPUTS</span></span>

### <span data-ttu-id="6adb4-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="6adb4-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="6adb4-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6adb4-153">NOTES</span></span>

## <span data-ttu-id="6adb4-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6adb4-154">RELATED LINKS</span></span>