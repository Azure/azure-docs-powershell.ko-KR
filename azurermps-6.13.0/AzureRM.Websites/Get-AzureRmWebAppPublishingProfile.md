---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a59d747dd7ba91d69d364770c91baf1a21ffedd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529312"
---
# <span data-ttu-id="6be2d-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="6be2d-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="6be2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6be2d-102">SYNOPSIS</span></span>
<span data-ttu-id="6be2d-103">Azure Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6be2d-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6be2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6be2d-104">SYNTAX</span></span>

### <span data-ttu-id="6be2d-105">S1</span><span class="sxs-lookup"><span data-stu-id="6be2d-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6be2d-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="6be2d-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6be2d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6be2d-107">DESCRIPTION</span></span>
<span data-ttu-id="6be2d-108">**AzureRmWebAppPublishingProfile** Cmdlet은 Azure Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6be2d-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="6be2d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6be2d-109">EXAMPLES</span></span>

### <span data-ttu-id="6be2d-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="6be2d-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="6be2d-111">이 명령은 리소스 그룹 Default-ContosoWebApp에 연결 된 웹 앱 용 Ftp 형식의 게시 프로필을 가져와 지정 된 출력 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6be2d-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="6be2d-112">변수</span><span class="sxs-lookup"><span data-stu-id="6be2d-112">PARAMETERS</span></span>

### <span data-ttu-id="6be2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be2d-113">-DefaultProfile</span></span>
<span data-ttu-id="6be2d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6be2d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6be2d-115">-형식</span><span class="sxs-lookup"><span data-stu-id="6be2d-115">-Format</span></span>
<span data-ttu-id="6be2d-116">포맷할</span><span class="sxs-lookup"><span data-stu-id="6be2d-116">Format</span></span>

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

### <span data-ttu-id="6be2d-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="6be2d-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="6be2d-118">True 인 경우 재해 복구 끝점 포함</span><span class="sxs-lookup"><span data-stu-id="6be2d-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6be2d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="6be2d-119">-Name</span></span>
<span data-ttu-id="6be2d-120">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="6be2d-120">WebApp Name</span></span>

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

### <span data-ttu-id="6be2d-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="6be2d-121">-OutputFile</span></span>
<span data-ttu-id="6be2d-122">출력 파일</span><span class="sxs-lookup"><span data-stu-id="6be2d-122">Output File</span></span>

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

### <span data-ttu-id="6be2d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6be2d-123">-ResourceGroupName</span></span>
<span data-ttu-id="6be2d-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6be2d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="6be2d-125">-Web app</span><span class="sxs-lookup"><span data-stu-id="6be2d-125">-WebApp</span></span>
<span data-ttu-id="6be2d-126">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="6be2d-126">WebApp Object</span></span>

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

### <span data-ttu-id="6be2d-127">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="6be2d-127">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="6be2d-128">True 인 경우 재해 복구 끝점 포함</span><span class="sxs-lookup"><span data-stu-id="6be2d-128">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6be2d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be2d-129">CommonParameters</span></span>
<span data-ttu-id="6be2d-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6be2d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be2d-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6be2d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be2d-132">입력</span><span class="sxs-lookup"><span data-stu-id="6be2d-132">INPUTS</span></span>

### <span data-ttu-id="6be2d-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6be2d-133">System.String</span></span>

### <span data-ttu-id="6be2d-134">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="6be2d-134">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="6be2d-135">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6be2d-135">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="6be2d-136">출력</span><span class="sxs-lookup"><span data-stu-id="6be2d-136">OUTPUTS</span></span>

### <span data-ttu-id="6be2d-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6be2d-137">System.String</span></span>

## <span data-ttu-id="6be2d-138">상속자</span><span class="sxs-lookup"><span data-stu-id="6be2d-138">NOTES</span></span>

## <span data-ttu-id="6be2d-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6be2d-139">RELATED LINKS</span></span>

[<span data-ttu-id="6be2d-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6be2d-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="6be2d-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6be2d-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


