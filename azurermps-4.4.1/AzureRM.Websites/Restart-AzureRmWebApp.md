---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
ms.openlocfilehash: eb75a4fa0ebeb121cd39e591b8cb8d46909deb42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525451"
---
# <span data-ttu-id="161ae-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="161ae-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="161ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="161ae-102">SYNOPSIS</span></span>
<span data-ttu-id="161ae-103">Azure Web App을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="161ae-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="161ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="161ae-104">SYNTAX</span></span>

### <span data-ttu-id="161ae-105">S1</span><span class="sxs-lookup"><span data-stu-id="161ae-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="161ae-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="161ae-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="161ae-107">설명은</span><span class="sxs-lookup"><span data-stu-id="161ae-107">DESCRIPTION</span></span>
<span data-ttu-id="161ae-108">**AzureRmWebApp** cmdlet이 중지 된 다음 Azure Web App을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="161ae-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="161ae-109">웹 앱이 중지 된 상태 이면 Start-AzureRmWebApp cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="161ae-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="161ae-110">예제의</span><span class="sxs-lookup"><span data-stu-id="161ae-110">EXAMPLES</span></span>

### <span data-ttu-id="161ae-111">예제 1: 웹 앱 다시 시작</span><span class="sxs-lookup"><span data-stu-id="161ae-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="161ae-112">이 명령은 Default-WestUS 이라는 리소스 그룹에 속한 ContosoSite 라는 Azure Web App을 중지 한 다음 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="161ae-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="161ae-113">변수</span><span class="sxs-lookup"><span data-stu-id="161ae-113">PARAMETERS</span></span>

### <span data-ttu-id="161ae-114">-이름</span><span class="sxs-lookup"><span data-stu-id="161ae-114">-Name</span></span>
<span data-ttu-id="161ae-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="161ae-115">WebApp Name</span></span>

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

### <span data-ttu-id="161ae-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="161ae-116">-ResourceGroupName</span></span>
<span data-ttu-id="161ae-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="161ae-117">Resource Group Name</span></span>

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

### <span data-ttu-id="161ae-118">-Web app</span><span class="sxs-lookup"><span data-stu-id="161ae-118">-WebApp</span></span>
<span data-ttu-id="161ae-119">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="161ae-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="161ae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="161ae-120">-DefaultProfile</span></span>
<span data-ttu-id="161ae-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="161ae-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="161ae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="161ae-122">CommonParameters</span></span>
<span data-ttu-id="161ae-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="161ae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="161ae-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="161ae-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="161ae-125">입력</span><span class="sxs-lookup"><span data-stu-id="161ae-125">INPUTS</span></span>

### <span data-ttu-id="161ae-126">Site</span><span class="sxs-lookup"><span data-stu-id="161ae-126">Site</span></span>
<span data-ttu-id="161ae-127">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="161ae-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="161ae-128">출력</span><span class="sxs-lookup"><span data-stu-id="161ae-128">OUTPUTS</span></span>

## <span data-ttu-id="161ae-129">상속자</span><span class="sxs-lookup"><span data-stu-id="161ae-129">NOTES</span></span>

## <span data-ttu-id="161ae-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="161ae-130">RELATED LINKS</span></span>

[<span data-ttu-id="161ae-131">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="161ae-131">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="161ae-132">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="161ae-132">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="161ae-133">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="161ae-133">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="161ae-134">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="161ae-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="161ae-135">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="161ae-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


