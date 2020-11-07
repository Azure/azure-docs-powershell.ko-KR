---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: eb1f96eaf85e6a5e7234e09c319b2e0c1117d456
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880290"
---
# <span data-ttu-id="1706b-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1706b-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="1706b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1706b-102">SYNOPSIS</span></span>
<span data-ttu-id="1706b-103">지정 된 리소스 그룹의 Azure 웹 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1706b-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1706b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1706b-104">SYNTAX</span></span>

### <span data-ttu-id="1706b-105">S1</span><span class="sxs-lookup"><span data-stu-id="1706b-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1706b-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="1706b-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1706b-107">시스템이</span><span class="sxs-lookup"><span data-stu-id="1706b-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1706b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1706b-108">DESCRIPTION</span></span>
<span data-ttu-id="1706b-109">**AzureRmWebApp** Cmdlet은 Azure 웹 앱에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1706b-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="1706b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1706b-110">EXAMPLES</span></span>

### <span data-ttu-id="1706b-111">예제 1: 리소스 그룹에서 웹 앱 가져오기</span><span class="sxs-lookup"><span data-stu-id="1706b-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="1706b-112">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 ContosoSite 이라는 웹 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1706b-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1706b-113">변수</span><span class="sxs-lookup"><span data-stu-id="1706b-113">PARAMETERS</span></span>

### <span data-ttu-id="1706b-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1706b-114">-AppServicePlan</span></span>
<span data-ttu-id="1706b-115">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="1706b-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1706b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1706b-116">-DefaultProfile</span></span>
<span data-ttu-id="1706b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1706b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1706b-118">-위치</span><span class="sxs-lookup"><span data-stu-id="1706b-118">-Location</span></span>
<span data-ttu-id="1706b-119">Location</span><span class="sxs-lookup"><span data-stu-id="1706b-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1706b-120">-이름</span><span class="sxs-lookup"><span data-stu-id="1706b-120">-Name</span></span>
<span data-ttu-id="1706b-121">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="1706b-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1706b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1706b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1706b-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1706b-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1706b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1706b-124">CommonParameters</span></span>
<span data-ttu-id="1706b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1706b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1706b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1706b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1706b-127">입력</span><span class="sxs-lookup"><span data-stu-id="1706b-127">INPUTS</span></span>

### <span data-ttu-id="1706b-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1706b-128">System.String</span></span>

## <span data-ttu-id="1706b-129">출력</span><span class="sxs-lookup"><span data-stu-id="1706b-129">OUTPUTS</span></span>

### <span data-ttu-id="1706b-130">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="1706b-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="1706b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1706b-131">NOTES</span></span>

## <span data-ttu-id="1706b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1706b-132">RELATED LINKS</span></span>

[<span data-ttu-id="1706b-133">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1706b-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="1706b-134">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1706b-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="1706b-135">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1706b-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="1706b-136">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1706b-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="1706b-137">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1706b-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


