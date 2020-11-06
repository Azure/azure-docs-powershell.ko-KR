---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a05dfcbf509ccb68c0b928467a5695361a4916e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529052"
---
# <span data-ttu-id="51d1b-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="51d1b-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="51d1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="51d1b-103">Azure Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="51d1b-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51d1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51d1b-104">SYNTAX</span></span>

### <span data-ttu-id="51d1b-105">S1</span><span class="sxs-lookup"><span data-stu-id="51d1b-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51d1b-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="51d1b-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51d1b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="51d1b-107">DESCRIPTION</span></span>
<span data-ttu-id="51d1b-108">**AzureRmWebAppPublishingProfile** Cmdlet은 Azure Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="51d1b-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="51d1b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="51d1b-109">EXAMPLES</span></span>

### <span data-ttu-id="51d1b-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="51d1b-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="51d1b-111">이 명령은 리소스 그룹 Default-ContosoWebApp에 연결 된 웹 앱 용 Ftp 형식의 게시 프로필을 가져와 지정 된 출력 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="51d1b-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="51d1b-112">변수</span><span class="sxs-lookup"><span data-stu-id="51d1b-112">PARAMETERS</span></span>

### <span data-ttu-id="51d1b-113">-형식</span><span class="sxs-lookup"><span data-stu-id="51d1b-113">-Format</span></span>
<span data-ttu-id="51d1b-114">포맷할</span><span class="sxs-lookup"><span data-stu-id="51d1b-114">Format</span></span>

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

### <span data-ttu-id="51d1b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="51d1b-115">-Name</span></span>
<span data-ttu-id="51d1b-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="51d1b-116">WebApp Name</span></span>

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

### <span data-ttu-id="51d1b-117">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="51d1b-117">-OutputFile</span></span>
<span data-ttu-id="51d1b-118">출력 파일</span><span class="sxs-lookup"><span data-stu-id="51d1b-118">Output File</span></span>

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

### <span data-ttu-id="51d1b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51d1b-119">-ResourceGroupName</span></span>
<span data-ttu-id="51d1b-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="51d1b-120">Resource Group Name</span></span>

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

### <span data-ttu-id="51d1b-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="51d1b-121">-WebApp</span></span>
<span data-ttu-id="51d1b-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="51d1b-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51d1b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51d1b-123">-DefaultProfile</span></span>
<span data-ttu-id="51d1b-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51d1b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51d1b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d1b-125">CommonParameters</span></span>
<span data-ttu-id="51d1b-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51d1b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d1b-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51d1b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d1b-128">입력</span><span class="sxs-lookup"><span data-stu-id="51d1b-128">INPUTS</span></span>

### <span data-ttu-id="51d1b-129">Site</span><span class="sxs-lookup"><span data-stu-id="51d1b-129">Site</span></span>
<span data-ttu-id="51d1b-130">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="51d1b-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="51d1b-131">출력</span><span class="sxs-lookup"><span data-stu-id="51d1b-131">OUTPUTS</span></span>

## <span data-ttu-id="51d1b-132">상속자</span><span class="sxs-lookup"><span data-stu-id="51d1b-132">NOTES</span></span>

## <span data-ttu-id="51d1b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51d1b-133">RELATED LINKS</span></span>

[<span data-ttu-id="51d1b-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="51d1b-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="51d1b-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="51d1b-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


