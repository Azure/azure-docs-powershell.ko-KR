---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: ed7ad2edb0c82203f571edccf9b6672428956ac2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698360"
---
# <span data-ttu-id="de955-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="de955-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="de955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de955-102">SYNOPSIS</span></span>
<span data-ttu-id="de955-103">Get-AzWebAppContainerContinuousDeploymentUrl에서 컨테이너 연속 배포 url을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="de955-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="de955-104">구문과</span><span class="sxs-lookup"><span data-stu-id="de955-104">SYNTAX</span></span>

### <span data-ttu-id="de955-105">S1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="de955-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de955-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="de955-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de955-107">설명은</span><span class="sxs-lookup"><span data-stu-id="de955-107">DESCRIPTION</span></span>
<span data-ttu-id="de955-108">Get-AzWebAppContainerContinuousDeploymentUrl에서 컨테이너 연속 배포 url을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="de955-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="de955-109">예제의</span><span class="sxs-lookup"><span data-stu-id="de955-109">EXAMPLES</span></span>

### <span data-ttu-id="de955-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="de955-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="de955-111">이 명령은 컨테이너 연속 배포 url을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="de955-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="de955-112">변수</span><span class="sxs-lookup"><span data-stu-id="de955-112">PARAMETERS</span></span>

### <span data-ttu-id="de955-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de955-113">-DefaultProfile</span></span>
<span data-ttu-id="de955-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="de955-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de955-115">-이름</span><span class="sxs-lookup"><span data-stu-id="de955-115">-Name</span></span>
<span data-ttu-id="de955-116">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="de955-116">The name of the web app.</span></span>

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

### <span data-ttu-id="de955-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de955-117">-ResourceGroupName</span></span>
<span data-ttu-id="de955-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="de955-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="de955-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="de955-119">-SlotName</span></span>
<span data-ttu-id="de955-120">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="de955-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="de955-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="de955-121">-WebApp</span></span>
<span data-ttu-id="de955-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="de955-122">The web app object</span></span>

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

### <span data-ttu-id="de955-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de955-123">CommonParameters</span></span>
<span data-ttu-id="de955-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="de955-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de955-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de955-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de955-126">입력</span><span class="sxs-lookup"><span data-stu-id="de955-126">INPUTS</span></span>

### <span data-ttu-id="de955-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="de955-127">System.String</span></span>

### <span data-ttu-id="de955-128">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="de955-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="de955-129">출력</span><span class="sxs-lookup"><span data-stu-id="de955-129">OUTPUTS</span></span>

### <span data-ttu-id="de955-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="de955-130">System.String</span></span>

## <span data-ttu-id="de955-131">상속자</span><span class="sxs-lookup"><span data-stu-id="de955-131">NOTES</span></span>

## <span data-ttu-id="de955-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de955-132">RELATED LINKS</span></span>
