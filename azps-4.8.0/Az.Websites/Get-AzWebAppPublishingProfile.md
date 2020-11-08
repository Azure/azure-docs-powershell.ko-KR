---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 4e4e8e1575070f04a02496014ab93276a2dc9328
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213126"
---
# <span data-ttu-id="f53ed-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="f53ed-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="f53ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f53ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f53ed-103">Azure Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f53ed-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="f53ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f53ed-104">SYNTAX</span></span>

### <span data-ttu-id="f53ed-105">S1</span><span class="sxs-lookup"><span data-stu-id="f53ed-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f53ed-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="f53ed-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f53ed-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f53ed-107">DESCRIPTION</span></span>
<span data-ttu-id="f53ed-108">**AzWebAppPublishingProfile** Cmdlet은 Azure Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f53ed-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="f53ed-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f53ed-109">EXAMPLES</span></span>

### <span data-ttu-id="f53ed-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f53ed-110">Example 1</span></span>
```powershell
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="f53ed-111">이 명령은 리소스 그룹 Default-ContosoWebApp에 연결 된 웹 앱 용 Ftp 형식의 게시 프로필을 가져와 지정 된 출력 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f53ed-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="f53ed-112">변수</span><span class="sxs-lookup"><span data-stu-id="f53ed-112">PARAMETERS</span></span>

### <span data-ttu-id="f53ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53ed-113">-DefaultProfile</span></span>
<span data-ttu-id="f53ed-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f53ed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f53ed-115">-형식</span><span class="sxs-lookup"><span data-stu-id="f53ed-115">-Format</span></span>
<span data-ttu-id="f53ed-116">포맷할</span><span class="sxs-lookup"><span data-stu-id="f53ed-116">Format</span></span>

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

### <span data-ttu-id="f53ed-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="f53ed-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="f53ed-118">True 인 경우 재해 복구 끝점 포함</span><span class="sxs-lookup"><span data-stu-id="f53ed-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="f53ed-119">-이름</span><span class="sxs-lookup"><span data-stu-id="f53ed-119">-Name</span></span>
<span data-ttu-id="f53ed-120">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="f53ed-120">WebApp Name</span></span>

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

### <span data-ttu-id="f53ed-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="f53ed-121">-OutputFile</span></span>
<span data-ttu-id="f53ed-122">출력 파일</span><span class="sxs-lookup"><span data-stu-id="f53ed-122">Output File</span></span>

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

### <span data-ttu-id="f53ed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f53ed-123">-ResourceGroupName</span></span>
<span data-ttu-id="f53ed-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f53ed-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f53ed-125">-Web app</span><span class="sxs-lookup"><span data-stu-id="f53ed-125">-WebApp</span></span>
<span data-ttu-id="f53ed-126">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="f53ed-126">WebApp Object</span></span>

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

### <span data-ttu-id="f53ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53ed-127">CommonParameters</span></span>
<span data-ttu-id="f53ed-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f53ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53ed-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f53ed-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53ed-130">입력</span><span class="sxs-lookup"><span data-stu-id="f53ed-130">INPUTS</span></span>

### <span data-ttu-id="f53ed-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f53ed-131">System.String</span></span>

### <span data-ttu-id="f53ed-132">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="f53ed-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f53ed-133">출력</span><span class="sxs-lookup"><span data-stu-id="f53ed-133">OUTPUTS</span></span>

### <span data-ttu-id="f53ed-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f53ed-134">System.String</span></span>

## <span data-ttu-id="f53ed-135">상속자</span><span class="sxs-lookup"><span data-stu-id="f53ed-135">NOTES</span></span>

## <span data-ttu-id="f53ed-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f53ed-136">RELATED LINKS</span></span>

[<span data-ttu-id="f53ed-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f53ed-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="f53ed-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f53ed-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


