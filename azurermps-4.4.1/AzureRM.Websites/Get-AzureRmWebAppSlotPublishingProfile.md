---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: d8ccd8f1011a73068c24323bb86e39340dfc9573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529970"
---
# <span data-ttu-id="91fcc-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="91fcc-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="91fcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="91fcc-103">Azure 웹 앱 슬롯 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91fcc-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91fcc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91fcc-104">SYNTAX</span></span>

### <span data-ttu-id="91fcc-105">S1</span><span class="sxs-lookup"><span data-stu-id="91fcc-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91fcc-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="91fcc-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91fcc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="91fcc-107">DESCRIPTION</span></span>
<span data-ttu-id="91fcc-108">**AzureRmWebAppSlotPublishingProfile** cmdlet은 지정 된 슬롯에 대 한 Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91fcc-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="91fcc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="91fcc-109">EXAMPLES</span></span>

### <span data-ttu-id="91fcc-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="91fcc-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="91fcc-111">이 명령은 리소스 그룹 Default-Slot001에 연결 된 웹 앱 ContosoWebApp에 대 한 게시 프로필을 Ftp 형식으로 가져와 지정 된 출력 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="91fcc-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="91fcc-112">변수</span><span class="sxs-lookup"><span data-stu-id="91fcc-112">PARAMETERS</span></span>

### <span data-ttu-id="91fcc-113">-형식</span><span class="sxs-lookup"><span data-stu-id="91fcc-113">-Format</span></span>
<span data-ttu-id="91fcc-114">포맷할</span><span class="sxs-lookup"><span data-stu-id="91fcc-114">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91fcc-115">-이름</span><span class="sxs-lookup"><span data-stu-id="91fcc-115">-Name</span></span>
<span data-ttu-id="91fcc-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="91fcc-116">WebApp Name</span></span>

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

### <span data-ttu-id="91fcc-117">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="91fcc-117">-OutputFile</span></span>
<span data-ttu-id="91fcc-118">출력 파일</span><span class="sxs-lookup"><span data-stu-id="91fcc-118">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91fcc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91fcc-119">-ResourceGroupName</span></span>
<span data-ttu-id="91fcc-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="91fcc-120">Resource Group Name</span></span>

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

### <span data-ttu-id="91fcc-121">-슬롯</span><span class="sxs-lookup"><span data-stu-id="91fcc-121">-Slot</span></span>
<span data-ttu-id="91fcc-122">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="91fcc-122">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91fcc-123">-Web app</span><span class="sxs-lookup"><span data-stu-id="91fcc-123">-WebApp</span></span>
<span data-ttu-id="91fcc-124">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="91fcc-124">WebApp Object</span></span>

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

### <span data-ttu-id="91fcc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91fcc-125">-DefaultProfile</span></span>
<span data-ttu-id="91fcc-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91fcc-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91fcc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91fcc-127">CommonParameters</span></span>
<span data-ttu-id="91fcc-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91fcc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91fcc-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91fcc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91fcc-130">입력</span><span class="sxs-lookup"><span data-stu-id="91fcc-130">INPUTS</span></span>

### <span data-ttu-id="91fcc-131">Site</span><span class="sxs-lookup"><span data-stu-id="91fcc-131">Site</span></span>
<span data-ttu-id="91fcc-132">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="91fcc-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="91fcc-133">출력</span><span class="sxs-lookup"><span data-stu-id="91fcc-133">OUTPUTS</span></span>

## <span data-ttu-id="91fcc-134">상속자</span><span class="sxs-lookup"><span data-stu-id="91fcc-134">NOTES</span></span>

## <span data-ttu-id="91fcc-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91fcc-135">RELATED LINKS</span></span>

[<span data-ttu-id="91fcc-136">다시 설정-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="91fcc-136">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="91fcc-137">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="91fcc-137">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="91fcc-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91fcc-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
