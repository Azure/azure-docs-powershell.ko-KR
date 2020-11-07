---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: cedaf16333d69a25dce0ce2657640e723767aece
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876141"
---
# <span data-ttu-id="2d027-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="2d027-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="2d027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d027-102">SYNOPSIS</span></span>
<span data-ttu-id="2d027-103">Azure 웹 앱 슬롯 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d027-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="2d027-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d027-104">SYNTAX</span></span>

### <span data-ttu-id="2d027-105">S1</span><span class="sxs-lookup"><span data-stu-id="2d027-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d027-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="2d027-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d027-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2d027-107">DESCRIPTION</span></span>
<span data-ttu-id="2d027-108">**AzWebAppSlotPublishingProfile** cmdlet은 지정 된 슬롯에 대 한 Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d027-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="2d027-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2d027-109">EXAMPLES</span></span>

### <span data-ttu-id="2d027-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2d027-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="2d027-111">이 명령은 리소스 그룹 Default-Slot001에 연결 된 웹 앱 ContosoWebApp에 대 한 게시 프로필을 Ftp 형식으로 가져와 지정 된 출력 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d027-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="2d027-112">변수</span><span class="sxs-lookup"><span data-stu-id="2d027-112">PARAMETERS</span></span>

### <span data-ttu-id="2d027-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d027-113">-DefaultProfile</span></span>
<span data-ttu-id="2d027-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d027-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d027-115">-형식</span><span class="sxs-lookup"><span data-stu-id="2d027-115">-Format</span></span>
<span data-ttu-id="2d027-116">포맷할</span><span class="sxs-lookup"><span data-stu-id="2d027-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d027-117">-이름</span><span class="sxs-lookup"><span data-stu-id="2d027-117">-Name</span></span>
<span data-ttu-id="2d027-118">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="2d027-118">WebApp Name</span></span>

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

### <span data-ttu-id="2d027-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="2d027-119">-OutputFile</span></span>
<span data-ttu-id="2d027-120">출력 파일</span><span class="sxs-lookup"><span data-stu-id="2d027-120">Output File</span></span>

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

### <span data-ttu-id="2d027-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d027-121">-ResourceGroupName</span></span>
<span data-ttu-id="2d027-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2d027-122">Resource Group Name</span></span>

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

### <span data-ttu-id="2d027-123">-슬롯</span><span class="sxs-lookup"><span data-stu-id="2d027-123">-Slot</span></span>
<span data-ttu-id="2d027-124">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="2d027-124">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d027-125">-Web app</span><span class="sxs-lookup"><span data-stu-id="2d027-125">-WebApp</span></span>
<span data-ttu-id="2d027-126">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="2d027-126">WebApp Object</span></span>

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

### <span data-ttu-id="2d027-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d027-127">CommonParameters</span></span>
<span data-ttu-id="2d027-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d027-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d027-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d027-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d027-130">입력</span><span class="sxs-lookup"><span data-stu-id="2d027-130">INPUTS</span></span>

### <span data-ttu-id="2d027-131">Site</span><span class="sxs-lookup"><span data-stu-id="2d027-131">Site</span></span>
<span data-ttu-id="2d027-132">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d027-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2d027-133">출력</span><span class="sxs-lookup"><span data-stu-id="2d027-133">OUTPUTS</span></span>

## <span data-ttu-id="2d027-134">상속자</span><span class="sxs-lookup"><span data-stu-id="2d027-134">NOTES</span></span>

## <span data-ttu-id="2d027-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d027-135">RELATED LINKS</span></span>

[<span data-ttu-id="2d027-136">다시 설정-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="2d027-136">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="2d027-137">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2d027-137">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="2d027-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2d027-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
