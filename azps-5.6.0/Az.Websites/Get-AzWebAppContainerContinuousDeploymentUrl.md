---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 90aca2939721144500519329492e04786b67a93a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981755"
---
# <span data-ttu-id="27739-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="27739-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="27739-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27739-102">SYNOPSIS</span></span>
<span data-ttu-id="27739-103">Get-AzWebAppContainerContinuousDeploymentUrl 컨테이너 연속 배포 URL을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="27739-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="27739-104">구문</span><span class="sxs-lookup"><span data-stu-id="27739-104">SYNTAX</span></span>

### <span data-ttu-id="27739-105">S1(기본값)</span><span class="sxs-lookup"><span data-stu-id="27739-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27739-106">S2</span><span class="sxs-lookup"><span data-stu-id="27739-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27739-107">설명</span><span class="sxs-lookup"><span data-stu-id="27739-107">DESCRIPTION</span></span>
<span data-ttu-id="27739-108">Get-AzWebAppContainerContinuousDeploymentUrl 컨테이너 연속 배포 URL을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="27739-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="27739-109">예제</span><span class="sxs-lookup"><span data-stu-id="27739-109">EXAMPLES</span></span>

### <span data-ttu-id="27739-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="27739-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="27739-111">이 명령은 컨테이너 연속 배포 URL을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="27739-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="27739-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="27739-112">PARAMETERS</span></span>

### <span data-ttu-id="27739-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27739-113">-DefaultProfile</span></span>
<span data-ttu-id="27739-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27739-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27739-115">-Name</span><span class="sxs-lookup"><span data-stu-id="27739-115">-Name</span></span>
<span data-ttu-id="27739-116">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27739-116">The name of the web app.</span></span>

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

### <span data-ttu-id="27739-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27739-117">-ResourceGroupName</span></span>
<span data-ttu-id="27739-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27739-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="27739-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="27739-119">-SlotName</span></span>
<span data-ttu-id="27739-120">웹앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27739-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="27739-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="27739-121">-WebApp</span></span>
<span data-ttu-id="27739-122">웹앱 개체</span><span class="sxs-lookup"><span data-stu-id="27739-122">The web app object</span></span>

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

### <span data-ttu-id="27739-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27739-123">CommonParameters</span></span>
<span data-ttu-id="27739-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27739-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27739-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="27739-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27739-126">입력</span><span class="sxs-lookup"><span data-stu-id="27739-126">INPUTS</span></span>

### <span data-ttu-id="27739-127">System.String</span><span class="sxs-lookup"><span data-stu-id="27739-127">System.String</span></span>

### <span data-ttu-id="27739-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="27739-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="27739-129">출력</span><span class="sxs-lookup"><span data-stu-id="27739-129">OUTPUTS</span></span>

### <span data-ttu-id="27739-130">System.String</span><span class="sxs-lookup"><span data-stu-id="27739-130">System.String</span></span>

## <span data-ttu-id="27739-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27739-131">NOTES</span></span>

## <span data-ttu-id="27739-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27739-132">RELATED LINKS</span></span>
