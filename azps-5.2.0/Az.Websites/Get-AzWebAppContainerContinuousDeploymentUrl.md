---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327130"
---
# <span data-ttu-id="08c6e-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="08c6e-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="08c6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="08c6e-103">Get-AzWebAppContainerContinuousDeploymentUrl 컨테이너 연속 배포 URL을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="08c6e-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="08c6e-104">구문</span><span class="sxs-lookup"><span data-stu-id="08c6e-104">SYNTAX</span></span>

### <span data-ttu-id="08c6e-105">S1(기본값)</span><span class="sxs-lookup"><span data-stu-id="08c6e-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08c6e-106">S2</span><span class="sxs-lookup"><span data-stu-id="08c6e-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08c6e-107">설명</span><span class="sxs-lookup"><span data-stu-id="08c6e-107">DESCRIPTION</span></span>
<span data-ttu-id="08c6e-108">Get-AzWebAppContainerContinuousDeploymentUrl 컨테이너 연속 배포 URL을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="08c6e-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="08c6e-109">예제</span><span class="sxs-lookup"><span data-stu-id="08c6e-109">EXAMPLES</span></span>

### <span data-ttu-id="08c6e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="08c6e-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="08c6e-111">이 명령은 컨테이너 연속 배포 URL을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="08c6e-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="08c6e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08c6e-112">PARAMETERS</span></span>

### <span data-ttu-id="08c6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c6e-113">-DefaultProfile</span></span>
<span data-ttu-id="08c6e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08c6e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08c6e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="08c6e-115">-Name</span></span>
<span data-ttu-id="08c6e-116">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08c6e-116">The name of the web app.</span></span>

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

### <span data-ttu-id="08c6e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08c6e-117">-ResourceGroupName</span></span>
<span data-ttu-id="08c6e-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08c6e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="08c6e-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="08c6e-119">-SlotName</span></span>
<span data-ttu-id="08c6e-120">웹앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08c6e-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="08c6e-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="08c6e-121">-WebApp</span></span>
<span data-ttu-id="08c6e-122">웹앱 개체</span><span class="sxs-lookup"><span data-stu-id="08c6e-122">The web app object</span></span>

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

### <span data-ttu-id="08c6e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c6e-123">CommonParameters</span></span>
<span data-ttu-id="08c6e-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="08c6e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c6e-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="08c6e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c6e-126">입력</span><span class="sxs-lookup"><span data-stu-id="08c6e-126">INPUTS</span></span>

### <span data-ttu-id="08c6e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="08c6e-127">System.String</span></span>

### <span data-ttu-id="08c6e-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="08c6e-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="08c6e-129">출력</span><span class="sxs-lookup"><span data-stu-id="08c6e-129">OUTPUTS</span></span>

### <span data-ttu-id="08c6e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="08c6e-130">System.String</span></span>

## <span data-ttu-id="08c6e-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="08c6e-131">NOTES</span></span>

## <span data-ttu-id="08c6e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08c6e-132">RELATED LINKS</span></span>
