---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: a89ebd3142d738664cd80cab198bd6f791c1287a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698353"
---
# <span data-ttu-id="97864-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="97864-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="97864-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97864-102">SYNOPSIS</span></span>
<span data-ttu-id="97864-103">Azure Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97864-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="97864-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97864-104">SYNTAX</span></span>

### <span data-ttu-id="97864-105">S1</span><span class="sxs-lookup"><span data-stu-id="97864-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97864-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="97864-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97864-107">설명은</span><span class="sxs-lookup"><span data-stu-id="97864-107">DESCRIPTION</span></span>
<span data-ttu-id="97864-108">**AzWebAppPublishingProfile** Cmdlet은 Azure Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97864-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="97864-109">예제의</span><span class="sxs-lookup"><span data-stu-id="97864-109">EXAMPLES</span></span>

### <span data-ttu-id="97864-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="97864-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="97864-111">이 명령은 리소스 그룹 Default-ContosoWebApp에 연결 된 웹 앱 용 Ftp 형식의 게시 프로필을 가져와 지정 된 출력 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="97864-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="97864-112">변수</span><span class="sxs-lookup"><span data-stu-id="97864-112">PARAMETERS</span></span>

### <span data-ttu-id="97864-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97864-113">-DefaultProfile</span></span>
<span data-ttu-id="97864-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97864-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97864-115">-형식</span><span class="sxs-lookup"><span data-stu-id="97864-115">-Format</span></span>
<span data-ttu-id="97864-116">포맷할</span><span class="sxs-lookup"><span data-stu-id="97864-116">Format</span></span>

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

### <span data-ttu-id="97864-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="97864-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="97864-118">True 인 경우 재해 복구 끝점 포함</span><span class="sxs-lookup"><span data-stu-id="97864-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="97864-119">-이름</span><span class="sxs-lookup"><span data-stu-id="97864-119">-Name</span></span>
<span data-ttu-id="97864-120">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="97864-120">WebApp Name</span></span>

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

### <span data-ttu-id="97864-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="97864-121">-OutputFile</span></span>
<span data-ttu-id="97864-122">출력 파일</span><span class="sxs-lookup"><span data-stu-id="97864-122">Output File</span></span>

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

### <span data-ttu-id="97864-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97864-123">-ResourceGroupName</span></span>
<span data-ttu-id="97864-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="97864-124">Resource Group Name</span></span>

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

### <span data-ttu-id="97864-125">-Web app</span><span class="sxs-lookup"><span data-stu-id="97864-125">-WebApp</span></span>
<span data-ttu-id="97864-126">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="97864-126">WebApp Object</span></span>

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

### <span data-ttu-id="97864-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97864-127">CommonParameters</span></span>
<span data-ttu-id="97864-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97864-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97864-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97864-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97864-130">입력</span><span class="sxs-lookup"><span data-stu-id="97864-130">INPUTS</span></span>

### <span data-ttu-id="97864-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="97864-131">System.String</span></span>

### <span data-ttu-id="97864-132">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="97864-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="97864-133">출력</span><span class="sxs-lookup"><span data-stu-id="97864-133">OUTPUTS</span></span>

### <span data-ttu-id="97864-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="97864-134">System.String</span></span>

## <span data-ttu-id="97864-135">상속자</span><span class="sxs-lookup"><span data-stu-id="97864-135">NOTES</span></span>

## <span data-ttu-id="97864-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97864-136">RELATED LINKS</span></span>

[<span data-ttu-id="97864-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="97864-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="97864-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="97864-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


