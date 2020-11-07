---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 477b60400082954eb12bd0756fb4380ece2a35ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876146"
---
# <span data-ttu-id="ab6a7-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ab6a7-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="ab6a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab6a7-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6a7-103">Azure Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab6a7-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="ab6a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab6a7-104">SYNTAX</span></span>

### <span data-ttu-id="ab6a7-105">S1</span><span class="sxs-lookup"><span data-stu-id="ab6a7-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab6a7-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="ab6a7-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab6a7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ab6a7-107">DESCRIPTION</span></span>
<span data-ttu-id="ab6a7-108">**AzWebAppPublishingProfile** Cmdlet은 Azure Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab6a7-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="ab6a7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ab6a7-109">EXAMPLES</span></span>

### <span data-ttu-id="ab6a7-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="ab6a7-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="ab6a7-111">이 명령은 리소스 그룹 Default-ContosoWebApp에 연결 된 웹 앱 용 Ftp 형식의 게시 프로필을 가져와 지정 된 출력 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6a7-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="ab6a7-112">변수</span><span class="sxs-lookup"><span data-stu-id="ab6a7-112">PARAMETERS</span></span>

### <span data-ttu-id="ab6a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6a7-113">-DefaultProfile</span></span>
<span data-ttu-id="ab6a7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab6a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab6a7-115">-형식</span><span class="sxs-lookup"><span data-stu-id="ab6a7-115">-Format</span></span>
<span data-ttu-id="ab6a7-116">포맷할</span><span class="sxs-lookup"><span data-stu-id="ab6a7-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab6a7-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ab6a7-117">-Name</span></span>
<span data-ttu-id="ab6a7-118">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="ab6a7-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6a7-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="ab6a7-119">-OutputFile</span></span>
<span data-ttu-id="ab6a7-120">출력 파일</span><span class="sxs-lookup"><span data-stu-id="ab6a7-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab6a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab6a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="ab6a7-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ab6a7-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab6a7-123">-Web app</span><span class="sxs-lookup"><span data-stu-id="ab6a7-123">-WebApp</span></span>
<span data-ttu-id="ab6a7-124">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="ab6a7-124">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6a7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6a7-125">CommonParameters</span></span>
<span data-ttu-id="ab6a7-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6a7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6a7-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab6a7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6a7-128">입력</span><span class="sxs-lookup"><span data-stu-id="ab6a7-128">INPUTS</span></span>

### <span data-ttu-id="ab6a7-129">Site</span><span class="sxs-lookup"><span data-stu-id="ab6a7-129">Site</span></span>
<span data-ttu-id="ab6a7-130">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6a7-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ab6a7-131">출력</span><span class="sxs-lookup"><span data-stu-id="ab6a7-131">OUTPUTS</span></span>

## <span data-ttu-id="ab6a7-132">상속자</span><span class="sxs-lookup"><span data-stu-id="ab6a7-132">NOTES</span></span>

## <span data-ttu-id="ab6a7-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab6a7-133">RELATED LINKS</span></span>

[<span data-ttu-id="ab6a7-134">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ab6a7-134">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="ab6a7-135">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab6a7-135">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


