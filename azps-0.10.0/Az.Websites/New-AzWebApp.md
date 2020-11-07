---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: ec5f9cf60025e6b35248b2e7f8058040b404ec42
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876140"
---
# <span data-ttu-id="97bed-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="97bed-101">New-AzWebApp</span></span>

## <span data-ttu-id="97bed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97bed-102">SYNOPSIS</span></span>
<span data-ttu-id="97bed-103">Azure Web App을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97bed-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="97bed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97bed-104">SYNTAX</span></span>

### <span data-ttu-id="97bed-105">SimpleParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="97bed-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-AsJob] [-GitRepositoryPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97bed-106">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="97bed-106">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [-SourceWebApp] <Site> [[-TrafficManagerProfile] <String>] [-IgnoreSourceControl]
 [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97bed-107">설명은</span><span class="sxs-lookup"><span data-stu-id="97bed-107">DESCRIPTION</span></span>
<span data-ttu-id="97bed-108">**AzWebApp** cmdlet은 지정 된 앱 서비스 계획 및 데이터 센터를 사용 하는 지정 된 리소스 그룹에서 Azure 웹 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97bed-108">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="97bed-109">예제의</span><span class="sxs-lookup"><span data-stu-id="97bed-109">EXAMPLES</span></span>

### <span data-ttu-id="97bed-110">예제 1: 웹 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="97bed-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="97bed-111">이 명령은 data center WestUS에서 Default-ContosoSite 이라는 기존 리소스 그룹의 Azure Web App (미국 이름)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97bed-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="97bed-112">이 명령은 ContosoServicePlan 이라는 기존 App Service 계획을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="97bed-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="97bed-113">변수</span><span class="sxs-lookup"><span data-stu-id="97bed-113">PARAMETERS</span></span>

### <span data-ttu-id="97bed-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="97bed-114">-AppServicePlan</span></span>
<span data-ttu-id="97bed-115">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="97bed-115">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="97bed-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="97bed-117">앱 설정이 HashTable를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="97bed-117">App Settings Overrides HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="97bed-118">-AseName</span></span>
<span data-ttu-id="97bed-119">App Service Environment 이름</span><span class="sxs-lookup"><span data-stu-id="97bed-119">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97bed-120">-AseResourceGroupName</span></span>
<span data-ttu-id="97bed-121">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="97bed-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97bed-122">-AsJob</span></span>
<span data-ttu-id="97bed-123">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="97bed-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97bed-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97bed-124">-DefaultProfile</span></span>
<span data-ttu-id="97bed-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97bed-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-126">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="97bed-126">-GitRepositoryPath</span></span>
<span data-ttu-id="97bed-127">배포할 웹 응용 프로그램 containign GitHub 리포지토리의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="97bed-127">Path to the GitHub repository containign the web application to deploy.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-128">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="97bed-128">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="97bed-129">사용자 지정 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="97bed-129">Ignore Custom Host Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-130">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="97bed-130">-IgnoreSourceControl</span></span>
<span data-ttu-id="97bed-131">원본 컨트롤 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="97bed-131">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-132">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="97bed-132">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="97bed-133">원본 Web app 슬롯 포함 옵션</span><span class="sxs-lookup"><span data-stu-id="97bed-133">Include Source WebApp Slots Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-134">-위치</span><span class="sxs-lookup"><span data-stu-id="97bed-134">-Location</span></span>
<span data-ttu-id="97bed-135">Location</span><span class="sxs-lookup"><span data-stu-id="97bed-135">Location</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-136">-이름</span><span class="sxs-lookup"><span data-stu-id="97bed-136">-Name</span></span>
<span data-ttu-id="97bed-137">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="97bed-137">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97bed-138">-ResourceGroupName</span></span>
<span data-ttu-id="97bed-139">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="97bed-139">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-140">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="97bed-140">-SourceWebApp</span></span>
<span data-ttu-id="97bed-141">원본 Web app 개체</span><span class="sxs-lookup"><span data-stu-id="97bed-141">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-142">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97bed-142">-TrafficManagerProfile</span></span>
<span data-ttu-id="97bed-143">기존 traffic manager 프로필의 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="97bed-143">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-144">-확인</span><span class="sxs-lookup"><span data-stu-id="97bed-144">-Confirm</span></span>
<span data-ttu-id="97bed-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="97bed-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97bed-146">-WhatIf</span></span>
<span data-ttu-id="97bed-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="97bed-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97bed-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="97bed-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97bed-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97bed-149">CommonParameters</span></span>
<span data-ttu-id="97bed-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97bed-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97bed-151">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97bed-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97bed-152">입력</span><span class="sxs-lookup"><span data-stu-id="97bed-152">INPUTS</span></span>

### <span data-ttu-id="97bed-153">Site</span><span class="sxs-lookup"><span data-stu-id="97bed-153">Site</span></span>
<span data-ttu-id="97bed-154">' SourceWebApp ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="97bed-154">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="97bed-155">출력</span><span class="sxs-lookup"><span data-stu-id="97bed-155">OUTPUTS</span></span>

### <span data-ttu-id="97bed-156">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="97bed-156">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="97bed-157">상속자</span><span class="sxs-lookup"><span data-stu-id="97bed-157">NOTES</span></span>

## <span data-ttu-id="97bed-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97bed-158">RELATED LINKS</span></span>

[<span data-ttu-id="97bed-159">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="97bed-159">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="97bed-160">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="97bed-160">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="97bed-161">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="97bed-161">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="97bed-162">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="97bed-162">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="97bed-163">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="97bed-163">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


