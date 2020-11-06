---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 4948de891815345efdc0b3f4ec39fb1874e510b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536916"
---
# <span data-ttu-id="92f1a-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92f1a-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="92f1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="92f1a-103">Azure Web App을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92f1a-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92f1a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92f1a-104">SYNTAX</span></span>

### <span data-ttu-id="92f1a-105">S1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="92f1a-105">S1 (Default)</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileId] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92f1a-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="92f1a-106">S2</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileName] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92f1a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="92f1a-107">DESCRIPTION</span></span>
<span data-ttu-id="92f1a-108">**AzureRmWebApp** cmdlet은 지정 된 앱 서비스 계획 및 데이터 센터를 사용 하는 지정 된 리소스 그룹에서 Azure 웹 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92f1a-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="92f1a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="92f1a-109">EXAMPLES</span></span>

### <span data-ttu-id="92f1a-110">예제 1: 웹 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="92f1a-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="92f1a-111">이 명령은 data center WestUS에서 Default-ContosoSite 이라는 기존 리소스 그룹의 Azure Web App (미국 이름)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92f1a-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="92f1a-112">이 명령은 ContosoServicePlan 이라는 기존 App Service 계획을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f1a-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="92f1a-113">변수</span><span class="sxs-lookup"><span data-stu-id="92f1a-113">PARAMETERS</span></span>

### <span data-ttu-id="92f1a-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="92f1a-114">-AppServicePlan</span></span>
<span data-ttu-id="92f1a-115">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="92f1a-115">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="92f1a-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="92f1a-117">앱 설정이 HashTable를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f1a-117">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="92f1a-118">-AseName</span></span>
<span data-ttu-id="92f1a-119">App Service Environment 이름</span><span class="sxs-lookup"><span data-stu-id="92f1a-119">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f1a-120">-AseResourceGroupName</span></span>
<span data-ttu-id="92f1a-121">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="92f1a-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="92f1a-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="92f1a-123">사용자 지정 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="92f1a-123">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="92f1a-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="92f1a-125">원본 컨트롤 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="92f1a-125">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-126">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="92f1a-126">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="92f1a-127">원본 Web app 슬롯 포함 옵션</span><span class="sxs-lookup"><span data-stu-id="92f1a-127">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-128">-위치</span><span class="sxs-lookup"><span data-stu-id="92f1a-128">-Location</span></span>
<span data-ttu-id="92f1a-129">Location</span><span class="sxs-lookup"><span data-stu-id="92f1a-129">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-130">-이름</span><span class="sxs-lookup"><span data-stu-id="92f1a-130">-Name</span></span>
<span data-ttu-id="92f1a-131">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="92f1a-131">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f1a-132">-ResourceGroupName</span></span>
<span data-ttu-id="92f1a-133">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="92f1a-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-134">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="92f1a-134">-SourceWebApp</span></span>
<span data-ttu-id="92f1a-135">원본 Web app 개체</span><span class="sxs-lookup"><span data-stu-id="92f1a-135">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-136">-TrafficManagerProfileId</span><span class="sxs-lookup"><span data-stu-id="92f1a-136">-TrafficManagerProfileId</span></span>
<span data-ttu-id="92f1a-137">Traffic Manager 프로필 Id</span><span class="sxs-lookup"><span data-stu-id="92f1a-137">Traffic Manager Profile Id</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-138">-TrafficManagerProfileName</span><span class="sxs-lookup"><span data-stu-id="92f1a-138">-TrafficManagerProfileName</span></span>
<span data-ttu-id="92f1a-139">Traffic Manager 프로필 이름</span><span class="sxs-lookup"><span data-stu-id="92f1a-139">Traffic Manager Profile Name</span></span>

```yaml
Type: System.String
Parameter Sets: S2
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f1a-140">-DefaultProfile</span></span>
<span data-ttu-id="92f1a-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92f1a-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f1a-142">CommonParameters</span></span>
<span data-ttu-id="92f1a-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f1a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f1a-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f1a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f1a-145">입력</span><span class="sxs-lookup"><span data-stu-id="92f1a-145">INPUTS</span></span>

### <span data-ttu-id="92f1a-146">Site</span><span class="sxs-lookup"><span data-stu-id="92f1a-146">Site</span></span>
<span data-ttu-id="92f1a-147">' SourceWebApp ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f1a-147">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="92f1a-148">출력</span><span class="sxs-lookup"><span data-stu-id="92f1a-148">OUTPUTS</span></span>

## <span data-ttu-id="92f1a-149">상속자</span><span class="sxs-lookup"><span data-stu-id="92f1a-149">NOTES</span></span>

## <span data-ttu-id="92f1a-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92f1a-150">RELATED LINKS</span></span>

[<span data-ttu-id="92f1a-151">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92f1a-151">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="92f1a-152">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92f1a-152">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="92f1a-153">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92f1a-153">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="92f1a-154">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92f1a-154">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="92f1a-155">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92f1a-155">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


