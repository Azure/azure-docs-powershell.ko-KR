---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 4e4e8e1575070f04a02496014ab93276a2dc9328
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208877"
---
# <span data-ttu-id="348a9-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="348a9-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="348a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="348a9-102">SYNOPSIS</span></span>
<span data-ttu-id="348a9-103">Azure 웹앱 게시 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="348a9-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="348a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="348a9-104">SYNTAX</span></span>

### <span data-ttu-id="348a9-105">S1</span><span class="sxs-lookup"><span data-stu-id="348a9-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="348a9-106">S2</span><span class="sxs-lookup"><span data-stu-id="348a9-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="348a9-107">설명</span><span class="sxs-lookup"><span data-stu-id="348a9-107">DESCRIPTION</span></span>
<span data-ttu-id="348a9-108">**Get-AzWebAppPublishingProfile** cmdlet은 Azure 웹앱 게시 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="348a9-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="348a9-109">예제</span><span class="sxs-lookup"><span data-stu-id="348a9-109">EXAMPLES</span></span>

### <span data-ttu-id="348a9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="348a9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="348a9-111">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 웹앱 ContosoWebApp에 대한 게시 프로필을 Ftp 형식으로 다운로드하고 지정된 출력 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="348a9-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="348a9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="348a9-112">PARAMETERS</span></span>

### <span data-ttu-id="348a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="348a9-113">-DefaultProfile</span></span>
<span data-ttu-id="348a9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="348a9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="348a9-115">-Format</span><span class="sxs-lookup"><span data-stu-id="348a9-115">-Format</span></span>
<span data-ttu-id="348a9-116">서식</span><span class="sxs-lookup"><span data-stu-id="348a9-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="348a9-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="348a9-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="348a9-118">true인 경우 재해 복구 엔드포인트 포함</span><span class="sxs-lookup"><span data-stu-id="348a9-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="348a9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="348a9-119">-Name</span></span>
<span data-ttu-id="348a9-120">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="348a9-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348a9-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="348a9-121">-OutputFile</span></span>
<span data-ttu-id="348a9-122">출력 파일</span><span class="sxs-lookup"><span data-stu-id="348a9-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="348a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="348a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="348a9-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="348a9-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="348a9-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="348a9-125">-WebApp</span></span>
<span data-ttu-id="348a9-126">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="348a9-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="348a9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="348a9-127">CommonParameters</span></span>
<span data-ttu-id="348a9-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="348a9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="348a9-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="348a9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="348a9-130">입력</span><span class="sxs-lookup"><span data-stu-id="348a9-130">INPUTS</span></span>

### <span data-ttu-id="348a9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="348a9-131">System.String</span></span>

### <span data-ttu-id="348a9-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="348a9-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="348a9-133">출력</span><span class="sxs-lookup"><span data-stu-id="348a9-133">OUTPUTS</span></span>

### <span data-ttu-id="348a9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="348a9-134">System.String</span></span>

## <span data-ttu-id="348a9-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="348a9-135">NOTES</span></span>

## <span data-ttu-id="348a9-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="348a9-136">RELATED LINKS</span></span>

[<span data-ttu-id="348a9-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="348a9-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="348a9-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="348a9-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


