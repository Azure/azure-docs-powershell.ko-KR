---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 64945cf503248fc0561dc894090c73d2d7151e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703076"
---
# <span data-ttu-id="9a357-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9a357-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="9a357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a357-102">SYNOPSIS</span></span>
<span data-ttu-id="9a357-103">지정 된 리소스 그룹의 Azure 웹 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a357-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a357-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a357-104">SYNTAX</span></span>

### <span data-ttu-id="9a357-105">S1</span><span class="sxs-lookup"><span data-stu-id="9a357-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a357-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="9a357-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a357-107">시스템이</span><span class="sxs-lookup"><span data-stu-id="9a357-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a357-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9a357-108">DESCRIPTION</span></span>
<span data-ttu-id="9a357-109">**AzureRmWebApp** Cmdlet은 Azure 웹 앱에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a357-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="9a357-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9a357-110">EXAMPLES</span></span>

### <span data-ttu-id="9a357-111">예제 1: 리소스 그룹에서 웹 앱 가져오기</span><span class="sxs-lookup"><span data-stu-id="9a357-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -SlotName "Slot001"
```

<span data-ttu-id="9a357-112">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 ContosoSite 이라는 웹 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a357-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9a357-113">변수</span><span class="sxs-lookup"><span data-stu-id="9a357-113">PARAMETERS</span></span>

### <span data-ttu-id="9a357-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9a357-114">-AppServicePlan</span></span>
<span data-ttu-id="9a357-115">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="9a357-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a357-116">-위치</span><span class="sxs-lookup"><span data-stu-id="9a357-116">-Location</span></span>
<span data-ttu-id="9a357-117">Location</span><span class="sxs-lookup"><span data-stu-id="9a357-117">Location</span></span>

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

### <span data-ttu-id="9a357-118">-이름</span><span class="sxs-lookup"><span data-stu-id="9a357-118">-Name</span></span>
<span data-ttu-id="9a357-119">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="9a357-119">WebApp Name</span></span>

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

### <span data-ttu-id="9a357-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a357-120">-ResourceGroupName</span></span>
<span data-ttu-id="9a357-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9a357-121">Resource Group Name</span></span>

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

### <span data-ttu-id="9a357-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a357-122">-DefaultProfile</span></span>
<span data-ttu-id="9a357-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a357-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a357-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a357-124">CommonParameters</span></span>
<span data-ttu-id="9a357-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a357-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a357-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a357-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a357-127">입력</span><span class="sxs-lookup"><span data-stu-id="9a357-127">INPUTS</span></span>

## <span data-ttu-id="9a357-128">출력</span><span class="sxs-lookup"><span data-stu-id="9a357-128">OUTPUTS</span></span>

## <span data-ttu-id="9a357-129">상속자</span><span class="sxs-lookup"><span data-stu-id="9a357-129">NOTES</span></span>

## <span data-ttu-id="9a357-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a357-130">RELATED LINKS</span></span>

[<span data-ttu-id="9a357-131">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9a357-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="9a357-132">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9a357-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="9a357-133">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9a357-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="9a357-134">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9a357-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="9a357-135">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9a357-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


