---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045877"
---
# <span data-ttu-id="6ec28-101">Publish-AzureWebsiteProject</span><span class="sxs-lookup"><span data-stu-id="6ec28-101">Publish-AzureWebsiteProject</span></span>

## <span data-ttu-id="6ec28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ec28-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec28-103">WebDeploy를 사용 하 여 Microsoft Azure 웹 사이트에 Visual Studio 웹 프로젝트를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-103">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>

## <span data-ttu-id="6ec28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ec28-104">SYNTAX</span></span>

### <span data-ttu-id="6ec28-105">ProjectFile</span><span class="sxs-lookup"><span data-stu-id="6ec28-105">ProjectFile</span></span>
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ec28-106">패키지할</span><span class="sxs-lookup"><span data-stu-id="6ec28-106">Package</span></span>
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6ec28-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6ec28-107">DESCRIPTION</span></span>
<span data-ttu-id="6ec28-108">WebDeploy를 사용 하 여 Microsoft Azure 웹 사이트에 Visual Studio 웹 프로젝트를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-108">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>
<span data-ttu-id="6ec28-109">WebDeploy 패키지를 사용 하 고 직접 게시 하거나 Visual Studio 웹 프로젝트를 가져와 프로젝트를 빌드하고 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-109">It can either take a WebDeploy package and publish directly, or take a Visual Studio web project, build the project and publish.</span></span>
<span data-ttu-id="6ec28-110">게시 하는 동안 Web.config의 연결 문자열을 바꿀 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-110">It can also replace the connection strings in the Web.config during publish.</span></span>

## <span data-ttu-id="6ec28-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6ec28-111">EXAMPLES</span></span>

### <span data-ttu-id="6ec28-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ec28-112">Example 1</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

<span data-ttu-id="6ec28-113">"디버그" 구성을 사용 하 여 Visual Studio 웹 프로젝트 빌드 (Web.Debug.config를 사용 하는 의미) 및 WebDeploy를 사용 하 여 Microsoft Azure 웹 사이트에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-113">Build a Visual Studio web project with "Debug" configuration (meaning use Web.Debug.config) and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="6ec28-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="6ec28-114">Example 2</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

<span data-ttu-id="6ec28-115">Webdeploy를 사용 하 여 WebDeploy 패키지 .zip 파일을 Microsoft Azure 웹 사이트에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-115">Publish a WebDeploy Package .zip file to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="6ec28-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="6ec28-116">Example 3</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

<span data-ttu-id="6ec28-117">Webdeploy를 사용 하 여 Microsoft Azure 웹 사이트에 WebDeploy 패키지 폴더를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-117">Publish a WebDeploy Package folder to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="6ec28-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="6ec28-118">Example 4</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

<span data-ttu-id="6ec28-119">Visual Studio 웹 프로젝트를 작성 하 고, Web.config에서 "DefaultConnection" 연결 문자열을 덮어쓰고, WebDeploy를 사용 하 여 Microsoft Azure 웹 사이트에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-119">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="6ec28-120">예제 5</span><span class="sxs-lookup"><span data-stu-id="6ec28-120">Example 5</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

<span data-ttu-id="6ec28-121">Visual Studio 웹 프로젝트를 작성 하 고, Web.config에서 "DefaultConnection" 연결 문자열을 덮어쓰고, WebDeploy를 사용 하 여 Microsoft Azure 웹 사이트에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-121">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>
<span data-ttu-id="6ec28-122">-DefaultConnection은 Web.config 구문 분석을 통해 추가 되는 동적 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-122">Notice that -DefaultConnection is a dynamic parameter which gets added by parsing Web.config.</span></span>

## <span data-ttu-id="6ec28-123">변수</span><span class="sxs-lookup"><span data-stu-id="6ec28-123">PARAMETERS</span></span>

### <span data-ttu-id="6ec28-124">-구성</span><span class="sxs-lookup"><span data-stu-id="6ec28-124">-Configuration</span></span>
<span data-ttu-id="6ec28-125">Visual Studio 웹 응용 프로그램 프로젝트를 빌드하는 데 사용 되는 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-125">The configuration used to build the Visual Studio web application project.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec28-126">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="6ec28-126">-ConnectionString</span></span>
<span data-ttu-id="6ec28-127">배포에 사용할 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-127">The connection strings to use for the deployment.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec28-128">-DoNotDelete</span><span class="sxs-lookup"><span data-stu-id="6ec28-128">-DoNotDelete</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec28-129">-이름</span><span class="sxs-lookup"><span data-stu-id="6ec28-129">-Name</span></span>
<span data-ttu-id="6ec28-130">웹 사이트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-130">The web site name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec28-131">-패키지</span><span class="sxs-lookup"><span data-stu-id="6ec28-131">-Package</span></span>
<span data-ttu-id="6ec28-132">게시할 Visual Studio 웹 응용 프로그램 프로젝트의 zip 파일에 대 한 WebDeploy 패키지 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-132">The WebDeploy package folder for zip file of the Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec28-133">-프로필</span><span class="sxs-lookup"><span data-stu-id="6ec28-133">-Profile</span></span>
<span data-ttu-id="6ec28-134">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6ec28-135">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec28-136">-ProjectFile</span><span class="sxs-lookup"><span data-stu-id="6ec28-136">-ProjectFile</span></span>
<span data-ttu-id="6ec28-137">게시할 Visual Studio 웹 응용 프로그램 프로젝트입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-137">The Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec28-138">-SetParametersFile</span><span class="sxs-lookup"><span data-stu-id="6ec28-138">-SetParametersFile</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec28-139">-SkipAppData</span><span class="sxs-lookup"><span data-stu-id="6ec28-139">-SkipAppData</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec28-140">-슬롯</span><span class="sxs-lookup"><span data-stu-id="6ec28-140">-Slot</span></span>
<span data-ttu-id="6ec28-141">웹 사이트 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-141">The web site slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec28-142">-토큰</span><span class="sxs-lookup"><span data-stu-id="6ec28-142">-Tokens</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec28-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec28-143">CommonParameters</span></span>
<span data-ttu-id="6ec28-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec28-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec28-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ec28-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec28-146">입력</span><span class="sxs-lookup"><span data-stu-id="6ec28-146">INPUTS</span></span>

## <span data-ttu-id="6ec28-147">출력</span><span class="sxs-lookup"><span data-stu-id="6ec28-147">OUTPUTS</span></span>

## <span data-ttu-id="6ec28-148">상속자</span><span class="sxs-lookup"><span data-stu-id="6ec28-148">NOTES</span></span>

## <span data-ttu-id="6ec28-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ec28-149">RELATED LINKS</span></span>

[<span data-ttu-id="6ec28-150">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6ec28-150">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="6ec28-151">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6ec28-151">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="6ec28-152">제거-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6ec28-152">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="6ec28-153">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6ec28-153">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


