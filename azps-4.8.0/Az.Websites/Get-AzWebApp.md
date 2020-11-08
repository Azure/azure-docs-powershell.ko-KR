---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 7dc1d2c5d6be1fd920ec9fb4eb90bf73b2c464b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213128"
---
# <span data-ttu-id="0392f-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0392f-101">Get-AzWebApp</span></span>

## <span data-ttu-id="0392f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0392f-102">SYNOPSIS</span></span>
<span data-ttu-id="0392f-103">지정 된 리소스 그룹의 Azure 웹 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0392f-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="0392f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0392f-104">SYNTAX</span></span>

### <span data-ttu-id="0392f-105">S1</span><span class="sxs-lookup"><span data-stu-id="0392f-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0392f-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="0392f-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0392f-107">시스템이</span><span class="sxs-lookup"><span data-stu-id="0392f-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0392f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0392f-108">DESCRIPTION</span></span>
<span data-ttu-id="0392f-109">**AzWebApp** Cmdlet은 Azure 웹 앱에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0392f-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="0392f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0392f-110">EXAMPLES</span></span>

### <span data-ttu-id="0392f-111">예제 1: 리소스 그룹에서 웹 앱 가져오기</span><span class="sxs-lookup"><span data-stu-id="0392f-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="0392f-112">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 ContosoSite 이라는 웹 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0392f-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0392f-113">변수</span><span class="sxs-lookup"><span data-stu-id="0392f-113">PARAMETERS</span></span>

### <span data-ttu-id="0392f-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0392f-114">-AppServicePlan</span></span>
<span data-ttu-id="0392f-115">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="0392f-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0392f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0392f-116">-DefaultProfile</span></span>
<span data-ttu-id="0392f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0392f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0392f-118">-위치</span><span class="sxs-lookup"><span data-stu-id="0392f-118">-Location</span></span>
<span data-ttu-id="0392f-119">Location</span><span class="sxs-lookup"><span data-stu-id="0392f-119">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0392f-120">-이름</span><span class="sxs-lookup"><span data-stu-id="0392f-120">-Name</span></span>
<span data-ttu-id="0392f-121">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="0392f-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0392f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0392f-122">-ResourceGroupName</span></span>
<span data-ttu-id="0392f-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0392f-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0392f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0392f-124">CommonParameters</span></span>
<span data-ttu-id="0392f-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0392f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0392f-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0392f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0392f-127">입력</span><span class="sxs-lookup"><span data-stu-id="0392f-127">INPUTS</span></span>

### <span data-ttu-id="0392f-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0392f-128">System.String</span></span>

## <span data-ttu-id="0392f-129">출력</span><span class="sxs-lookup"><span data-stu-id="0392f-129">OUTPUTS</span></span>

### <span data-ttu-id="0392f-130">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="0392f-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0392f-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0392f-131">NOTES</span></span>

## <span data-ttu-id="0392f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0392f-132">RELATED LINKS</span></span>

[<span data-ttu-id="0392f-133">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0392f-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="0392f-134">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0392f-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="0392f-135">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0392f-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="0392f-136">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0392f-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="0392f-137">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0392f-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


