---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 7dc1d2c5d6be1fd920ec9fb4eb90bf73b2c464b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182468"
---
# <span data-ttu-id="4b225-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4b225-101">Get-AzWebApp</span></span>

## <span data-ttu-id="4b225-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b225-102">SYNOPSIS</span></span>
<span data-ttu-id="4b225-103">지정된 리소스 그룹에서 Azure Web Apps를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b225-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="4b225-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b225-104">SYNTAX</span></span>

### <span data-ttu-id="4b225-105">S1</span><span class="sxs-lookup"><span data-stu-id="4b225-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b225-106">S2</span><span class="sxs-lookup"><span data-stu-id="4b225-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b225-107">S3</span><span class="sxs-lookup"><span data-stu-id="4b225-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b225-108">설명</span><span class="sxs-lookup"><span data-stu-id="4b225-108">DESCRIPTION</span></span>
<span data-ttu-id="4b225-109">**Get-AzWebApp** cmdlet은 Azure 웹앱에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b225-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="4b225-110">예제</span><span class="sxs-lookup"><span data-stu-id="4b225-110">EXAMPLES</span></span>

### <span data-ttu-id="4b225-111">예제 1: 리소스 그룹에서 웹앱 다운로드</span><span class="sxs-lookup"><span data-stu-id="4b225-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="4b225-112">이 명령은 리소스 그룹 Default-Web-WestUS에 속하는 ContosoSite라는 웹앱을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b225-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="4b225-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b225-113">PARAMETERS</span></span>

### <span data-ttu-id="4b225-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4b225-114">-AppServicePlan</span></span>
<span data-ttu-id="4b225-115">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="4b225-115">App Service Plan object</span></span>

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

### <span data-ttu-id="4b225-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b225-116">-DefaultProfile</span></span>
<span data-ttu-id="4b225-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b225-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b225-118">-Location</span><span class="sxs-lookup"><span data-stu-id="4b225-118">-Location</span></span>
<span data-ttu-id="4b225-119">위치</span><span class="sxs-lookup"><span data-stu-id="4b225-119">Location</span></span>

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

### <span data-ttu-id="4b225-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4b225-120">-Name</span></span>
<span data-ttu-id="4b225-121">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="4b225-121">WebApp Name</span></span>

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

### <span data-ttu-id="4b225-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b225-122">-ResourceGroupName</span></span>
<span data-ttu-id="4b225-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4b225-123">Resource Group Name</span></span>

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

### <span data-ttu-id="4b225-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b225-124">CommonParameters</span></span>
<span data-ttu-id="4b225-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b225-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b225-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4b225-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b225-127">입력</span><span class="sxs-lookup"><span data-stu-id="4b225-127">INPUTS</span></span>

### <span data-ttu-id="4b225-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4b225-128">System.String</span></span>

## <span data-ttu-id="4b225-129">출력</span><span class="sxs-lookup"><span data-stu-id="4b225-129">OUTPUTS</span></span>

### <span data-ttu-id="4b225-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="4b225-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4b225-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b225-131">NOTES</span></span>

## <span data-ttu-id="4b225-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b225-132">RELATED LINKS</span></span>

[<span data-ttu-id="4b225-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4b225-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="4b225-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4b225-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="4b225-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4b225-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="4b225-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4b225-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="4b225-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4b225-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


