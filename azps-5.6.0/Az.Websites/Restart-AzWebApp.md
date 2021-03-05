---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: e155a58420d9f190bfebdb21272d64dab1f3c21f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002096"
---
# <span data-ttu-id="731f6-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="731f6-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="731f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="731f6-102">SYNOPSIS</span></span>
<span data-ttu-id="731f6-103">Azure Web App을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="731f6-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="731f6-104">구문</span><span class="sxs-lookup"><span data-stu-id="731f6-104">SYNTAX</span></span>

### <span data-ttu-id="731f6-105">S1</span><span class="sxs-lookup"><span data-stu-id="731f6-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="731f6-106">S2</span><span class="sxs-lookup"><span data-stu-id="731f6-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="731f6-107">설명</span><span class="sxs-lookup"><span data-stu-id="731f6-107">DESCRIPTION</span></span>
<span data-ttu-id="731f6-108">**다시 시작-AzWebApp** cmdlet이 중지된 다음 Azure Web App을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="731f6-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="731f6-109">Web App이 중지된 상태인 경우 Start-AzWebApp cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="731f6-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="731f6-110">예제</span><span class="sxs-lookup"><span data-stu-id="731f6-110">EXAMPLES</span></span>

### <span data-ttu-id="731f6-111">예제 1: 웹앱 다시 시작</span><span class="sxs-lookup"><span data-stu-id="731f6-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="731f6-112">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoSite라는 Azure Web App을 중지한 다음 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="731f6-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="731f6-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="731f6-113">PARAMETERS</span></span>

### <span data-ttu-id="731f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="731f6-114">-DefaultProfile</span></span>
<span data-ttu-id="731f6-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="731f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="731f6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="731f6-116">-Name</span></span>
<span data-ttu-id="731f6-117">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="731f6-117">WebApp Name</span></span>

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

### <span data-ttu-id="731f6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="731f6-118">-ResourceGroupName</span></span>
<span data-ttu-id="731f6-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="731f6-119">Resource Group Name</span></span>

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

### <span data-ttu-id="731f6-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="731f6-120">-WebApp</span></span>
<span data-ttu-id="731f6-121">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="731f6-121">WebApp Object</span></span>

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

### <span data-ttu-id="731f6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731f6-122">CommonParameters</span></span>
<span data-ttu-id="731f6-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="731f6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731f6-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="731f6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731f6-125">입력</span><span class="sxs-lookup"><span data-stu-id="731f6-125">INPUTS</span></span>

### <span data-ttu-id="731f6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="731f6-126">System.String</span></span>

### <span data-ttu-id="731f6-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="731f6-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="731f6-128">출력</span><span class="sxs-lookup"><span data-stu-id="731f6-128">OUTPUTS</span></span>

### <span data-ttu-id="731f6-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="731f6-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="731f6-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="731f6-130">NOTES</span></span>

## <span data-ttu-id="731f6-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="731f6-131">RELATED LINKS</span></span>

[<span data-ttu-id="731f6-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="731f6-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="731f6-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="731f6-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="731f6-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="731f6-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="731f6-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="731f6-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="731f6-136">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="731f6-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


