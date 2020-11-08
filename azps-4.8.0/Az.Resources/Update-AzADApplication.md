---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: c4754ecf8cae06fd43f57bc50d3b3fbeaf1d5081
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214002"
---
# <span data-ttu-id="e8ba1-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e8ba1-101">Update-AzADApplication</span></span>

## <span data-ttu-id="e8ba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ba1-103">기존 azure active directory 응용 프로그램을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="e8ba1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e8ba1-104">SYNTAX</span></span>

### <span data-ttu-id="e8ba1-105">ApplicationObjectIdWithUpdateParamsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e8ba1-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ba1-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8ba1-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ba1-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8ba1-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8ba1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e8ba1-108">DESCRIPTION</span></span>
<span data-ttu-id="e8ba1-109">기존 azure active directory 응용 프로그램을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="e8ba1-110">이 응용 프로그램에 연결 된 자격 증명을 업데이트 하려면 New-AzADAppCredential cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="e8ba1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e8ba1-111">EXAMPLES</span></span>

### <span data-ttu-id="e8ba1-112">예제 1-응용 프로그램의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="e8ba1-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="e8ba1-113">개체 id가 ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 ' 인 응용 프로그램의 표시 이름을 ' MyNewDisplayName '로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="e8ba1-114">예제 2-응용 프로그램의 모든 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="e8ba1-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="e8ba1-115">개체 id가 ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 ' 인 응용 프로그램의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="e8ba1-116">예제 3-파이핑을 사용 하 여 응용 프로그램의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="e8ba1-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="e8ba1-117">개체 id가 ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 ' 인 응용 프로그램을 가져오고 응용 프로그램의 표시 이름을 "MyNewDisplayName"로 업데이트 하도록 Update-AzADApplication cmdlet에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="e8ba1-118">변수</span><span class="sxs-lookup"><span data-stu-id="e8ba1-118">PARAMETERS</span></span>

### <span data-ttu-id="e8ba1-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e8ba1-119">-ApplicationId</span></span>
<span data-ttu-id="e8ba1-120">업데이트할 응용 프로그램의 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="e8ba1-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="e8ba1-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="e8ba1-122">응용 프로그램이 다른 테 넌 트와 공유 되 면 True이 고, 그렇지 않으면 false입니다. 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="e8ba1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ba1-123">-DefaultProfile</span></span>
<span data-ttu-id="e8ba1-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8ba1-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e8ba1-125">-DisplayName</span></span>
<span data-ttu-id="e8ba1-126">업데이트할 응용 프로그램의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="e8ba1-127">-홈페이지</span><span class="sxs-lookup"><span data-stu-id="e8ba1-127">-HomePage</span></span>
<span data-ttu-id="e8ba1-128">응용 프로그램의 홈페이지에 대 한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="e8ba1-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="e8ba1-129">-IdentifierUri</span></span>
<span data-ttu-id="e8ba1-130">응용 프로그램을 식별 하는 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="e8ba1-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8ba1-131">-InputObject</span></span>
<span data-ttu-id="e8ba1-132">업데이트할 응용 프로그램을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-132">The object representing the application to update.</span></span>

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

### <span data-ttu-id="e8ba1-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e8ba1-133">-ObjectId</span></span>
<span data-ttu-id="e8ba1-134">업데이트할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-134">The object id of the application to update.</span></span>

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

### <span data-ttu-id="e8ba1-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="e8ba1-135">-ReplyUrl</span></span>
<span data-ttu-id="e8ba1-136">로그인을 위해 사용자 토큰이 전송 되는 Url 또는 OAuth 2.0 인증 코드 및 액세스 토큰이 전송 되는 리디렉션 Uri를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="e8ba1-137">-확인</span><span class="sxs-lookup"><span data-stu-id="e8ba1-137">-Confirm</span></span>
<span data-ttu-id="e8ba1-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ba1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ba1-139">-WhatIf</span></span>
<span data-ttu-id="e8ba1-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8ba1-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ba1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ba1-142">CommonParameters</span></span>
<span data-ttu-id="e8ba1-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ba1-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8ba1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ba1-145">입력</span><span class="sxs-lookup"><span data-stu-id="e8ba1-145">INPUTS</span></span>

### <span data-ttu-id="e8ba1-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e8ba1-146">System.String</span></span>

### <span data-ttu-id="e8ba1-147">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="e8ba1-147">System.Guid</span></span>

### <span data-ttu-id="e8ba1-148">ActiveDirectory PSADApplication 프로그램</span><span class="sxs-lookup"><span data-stu-id="e8ba1-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="e8ba1-149">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="e8ba1-149">System.String[]</span></span>

### <span data-ttu-id="e8ba1-150">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e8ba1-150">System.Boolean</span></span>

## <span data-ttu-id="e8ba1-151">출력</span><span class="sxs-lookup"><span data-stu-id="e8ba1-151">OUTPUTS</span></span>

### <span data-ttu-id="e8ba1-152">ActiveDirectory PSADApplication 프로그램</span><span class="sxs-lookup"><span data-stu-id="e8ba1-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e8ba1-153">상속자</span><span class="sxs-lookup"><span data-stu-id="e8ba1-153">NOTES</span></span>

## <span data-ttu-id="e8ba1-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8ba1-154">RELATED LINKS</span></span>
