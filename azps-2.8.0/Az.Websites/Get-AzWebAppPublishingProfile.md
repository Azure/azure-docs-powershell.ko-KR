---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 2ba74b42225646507d5bd081300405edfb9410fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874437"
---
# <span data-ttu-id="41ee4-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="41ee4-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="41ee4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="41ee4-103">Azure Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="41ee4-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="41ee4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41ee4-104">SYNTAX</span></span>

### <span data-ttu-id="41ee4-105">S1</span><span class="sxs-lookup"><span data-stu-id="41ee4-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41ee4-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="41ee4-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41ee4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="41ee4-107">DESCRIPTION</span></span>
<span data-ttu-id="41ee4-108">**AzWebAppPublishingProfile** Cmdlet은 Azure Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="41ee4-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="41ee4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="41ee4-109">EXAMPLES</span></span>

### <span data-ttu-id="41ee4-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="41ee4-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="41ee4-111">이 명령은 리소스 그룹 Default-ContosoWebApp에 연결 된 웹 앱 용 Ftp 형식의 게시 프로필을 가져와 지정 된 출력 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="41ee4-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="41ee4-112">변수</span><span class="sxs-lookup"><span data-stu-id="41ee4-112">PARAMETERS</span></span>

### <span data-ttu-id="41ee4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41ee4-113">-DefaultProfile</span></span>
<span data-ttu-id="41ee4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41ee4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41ee4-115">-형식</span><span class="sxs-lookup"><span data-stu-id="41ee4-115">-Format</span></span>
<span data-ttu-id="41ee4-116">포맷할</span><span class="sxs-lookup"><span data-stu-id="41ee4-116">Format</span></span>

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

### <span data-ttu-id="41ee4-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="41ee4-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="41ee4-118">True 인 경우 재해 복구 끝점 포함</span><span class="sxs-lookup"><span data-stu-id="41ee4-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="41ee4-119">-이름</span><span class="sxs-lookup"><span data-stu-id="41ee4-119">-Name</span></span>
<span data-ttu-id="41ee4-120">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="41ee4-120">WebApp Name</span></span>

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

### <span data-ttu-id="41ee4-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="41ee4-121">-OutputFile</span></span>
<span data-ttu-id="41ee4-122">출력 파일</span><span class="sxs-lookup"><span data-stu-id="41ee4-122">Output File</span></span>

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

### <span data-ttu-id="41ee4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41ee4-123">-ResourceGroupName</span></span>
<span data-ttu-id="41ee4-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="41ee4-124">Resource Group Name</span></span>

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

### <span data-ttu-id="41ee4-125">-Web app</span><span class="sxs-lookup"><span data-stu-id="41ee4-125">-WebApp</span></span>
<span data-ttu-id="41ee4-126">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="41ee4-126">WebApp Object</span></span>

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

### <span data-ttu-id="41ee4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ee4-127">CommonParameters</span></span>
<span data-ttu-id="41ee4-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41ee4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ee4-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41ee4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ee4-130">입력</span><span class="sxs-lookup"><span data-stu-id="41ee4-130">INPUTS</span></span>

### <span data-ttu-id="41ee4-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="41ee4-131">System.String</span></span>

### <span data-ttu-id="41ee4-132">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="41ee4-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="41ee4-133">출력</span><span class="sxs-lookup"><span data-stu-id="41ee4-133">OUTPUTS</span></span>

### <span data-ttu-id="41ee4-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="41ee4-134">System.String</span></span>

## <span data-ttu-id="41ee4-135">상속자</span><span class="sxs-lookup"><span data-stu-id="41ee4-135">NOTES</span></span>

## <span data-ttu-id="41ee4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41ee4-136">RELATED LINKS</span></span>

[<span data-ttu-id="41ee4-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="41ee4-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="41ee4-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41ee4-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


