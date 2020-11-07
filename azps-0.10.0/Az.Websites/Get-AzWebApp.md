---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: f86e0f18c7d793b5876a48c39b56b11c14b17546
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876161"
---
# <span data-ttu-id="8a6bf-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8a6bf-101">Get-AzWebApp</span></span>

## <span data-ttu-id="8a6bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6bf-103">지정 된 리소스 그룹의 Azure 웹 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="8a6bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a6bf-104">SYNTAX</span></span>

### <span data-ttu-id="8a6bf-105">S1</span><span class="sxs-lookup"><span data-stu-id="8a6bf-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a6bf-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="8a6bf-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a6bf-107">시스템이</span><span class="sxs-lookup"><span data-stu-id="8a6bf-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a6bf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8a6bf-108">DESCRIPTION</span></span>
<span data-ttu-id="8a6bf-109">**AzWebApp** Cmdlet은 Azure 웹 앱에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="8a6bf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8a6bf-110">EXAMPLES</span></span>

### <span data-ttu-id="8a6bf-111">예제 1: 리소스 그룹에서 웹 앱 가져오기</span><span class="sxs-lookup"><span data-stu-id="8a6bf-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="8a6bf-112">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 ContosoSite 이라는 웹 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8a6bf-113">변수</span><span class="sxs-lookup"><span data-stu-id="8a6bf-113">PARAMETERS</span></span>

### <span data-ttu-id="8a6bf-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8a6bf-114">-AppServicePlan</span></span>
<span data-ttu-id="8a6bf-115">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="8a6bf-115">App Service Plan object</span></span>

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

### <span data-ttu-id="8a6bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a6bf-116">-DefaultProfile</span></span>
<span data-ttu-id="8a6bf-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a6bf-118">-위치</span><span class="sxs-lookup"><span data-stu-id="8a6bf-118">-Location</span></span>
<span data-ttu-id="8a6bf-119">Location</span><span class="sxs-lookup"><span data-stu-id="8a6bf-119">Location</span></span>

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

### <span data-ttu-id="8a6bf-120">-이름</span><span class="sxs-lookup"><span data-stu-id="8a6bf-120">-Name</span></span>
<span data-ttu-id="8a6bf-121">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="8a6bf-121">WebApp Name</span></span>

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

### <span data-ttu-id="8a6bf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a6bf-122">-ResourceGroupName</span></span>
<span data-ttu-id="8a6bf-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8a6bf-123">Resource Group Name</span></span>

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

### <span data-ttu-id="8a6bf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6bf-124">CommonParameters</span></span>
<span data-ttu-id="8a6bf-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6bf-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a6bf-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6bf-127">입력</span><span class="sxs-lookup"><span data-stu-id="8a6bf-127">INPUTS</span></span>

### <span data-ttu-id="8a6bf-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8a6bf-128">System.String</span></span>

## <span data-ttu-id="8a6bf-129">출력</span><span class="sxs-lookup"><span data-stu-id="8a6bf-129">OUTPUTS</span></span>

### <span data-ttu-id="8a6bf-130">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="8a6bf-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="8a6bf-131">상속자</span><span class="sxs-lookup"><span data-stu-id="8a6bf-131">NOTES</span></span>

## <span data-ttu-id="8a6bf-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a6bf-132">RELATED LINKS</span></span>

[<span data-ttu-id="8a6bf-133">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8a6bf-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="8a6bf-134">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8a6bf-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="8a6bf-135">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8a6bf-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="8a6bf-136">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8a6bf-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="8a6bf-137">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8a6bf-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


