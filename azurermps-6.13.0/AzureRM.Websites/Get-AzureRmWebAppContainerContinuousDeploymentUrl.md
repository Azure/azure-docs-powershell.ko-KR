---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 0618b7c4cc4f9ee8b2342306e4aadf83ff0c17f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530026"
---
# <span data-ttu-id="02451-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="02451-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="02451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02451-102">SYNOPSIS</span></span>
<span data-ttu-id="02451-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl에서 컨테이너 연속 배포 url을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="02451-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02451-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02451-104">SYNTAX</span></span>

### <span data-ttu-id="02451-105">S1</span><span class="sxs-lookup"><span data-stu-id="02451-105">S1</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02451-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="02451-106">S2</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02451-107">설명은</span><span class="sxs-lookup"><span data-stu-id="02451-107">DESCRIPTION</span></span>
<span data-ttu-id="02451-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl에서 컨테이너 연속 배포 url을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="02451-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="02451-109">예제의</span><span class="sxs-lookup"><span data-stu-id="02451-109">EXAMPLES</span></span>

### <span data-ttu-id="02451-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="02451-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="02451-111">이 명령은 컨테이너 연속 배포 url을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="02451-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="02451-112">변수</span><span class="sxs-lookup"><span data-stu-id="02451-112">PARAMETERS</span></span>

### <span data-ttu-id="02451-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02451-113">-DefaultProfile</span></span>
<span data-ttu-id="02451-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02451-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02451-115">-이름</span><span class="sxs-lookup"><span data-stu-id="02451-115">-Name</span></span>
<span data-ttu-id="02451-116">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02451-116">The name of the web app.</span></span>

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

### <span data-ttu-id="02451-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02451-117">-ResourceGroupName</span></span>
<span data-ttu-id="02451-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02451-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="02451-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="02451-119">-SlotName</span></span>
<span data-ttu-id="02451-120">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02451-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="02451-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="02451-121">-WebApp</span></span>
<span data-ttu-id="02451-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="02451-122">The web app object</span></span>

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

### <span data-ttu-id="02451-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02451-123">CommonParameters</span></span>
<span data-ttu-id="02451-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02451-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02451-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02451-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02451-126">입력</span><span class="sxs-lookup"><span data-stu-id="02451-126">INPUTS</span></span>

### <span data-ttu-id="02451-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02451-127">System.String</span></span>
### <span data-ttu-id="02451-128">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="02451-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="02451-129">출력</span><span class="sxs-lookup"><span data-stu-id="02451-129">OUTPUTS</span></span>

### <span data-ttu-id="02451-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02451-130">System.String</span></span>
## <span data-ttu-id="02451-131">상속자</span><span class="sxs-lookup"><span data-stu-id="02451-131">NOTES</span></span>

## <span data-ttu-id="02451-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02451-132">RELATED LINKS</span></span>
