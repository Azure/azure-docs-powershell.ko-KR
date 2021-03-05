---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 00df9069400a1d3e2ae10abfb03d9d55bff08735
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972368"
---
# <span data-ttu-id="315fd-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="315fd-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="315fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="315fd-102">SYNOPSIS</span></span>

## <span data-ttu-id="315fd-103">구문</span><span class="sxs-lookup"><span data-stu-id="315fd-103">SYNTAX</span></span>

### <span data-ttu-id="315fd-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="315fd-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="315fd-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="315fd-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="315fd-106">설명</span><span class="sxs-lookup"><span data-stu-id="315fd-106">DESCRIPTION</span></span>
<span data-ttu-id="315fd-107">**Get-AzWebAppBackupConfiguration** cmdlet은 Azure Web App의 백업 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="315fd-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="315fd-108">예제</span><span class="sxs-lookup"><span data-stu-id="315fd-108">EXAMPLES</span></span>

### <span data-ttu-id="315fd-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="315fd-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="315fd-110">이 명령은 리소스 그룹 Default-Web-WestUS에 속하는 WebAppStandard라는 웹앱에서 백업 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="315fd-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="315fd-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="315fd-111">PARAMETERS</span></span>

### <span data-ttu-id="315fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="315fd-112">-DefaultProfile</span></span>
<span data-ttu-id="315fd-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="315fd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="315fd-114">-Name</span><span class="sxs-lookup"><span data-stu-id="315fd-114">-Name</span></span>
<span data-ttu-id="315fd-115">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="315fd-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="315fd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="315fd-116">-ResourceGroupName</span></span>
<span data-ttu-id="315fd-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="315fd-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="315fd-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="315fd-118">-Slot</span></span>
<span data-ttu-id="315fd-119">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="315fd-119">Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="315fd-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="315fd-120">-WebApp</span></span>
<span data-ttu-id="315fd-121">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="315fd-121">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="315fd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="315fd-122">CommonParameters</span></span>
<span data-ttu-id="315fd-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="315fd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="315fd-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="315fd-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="315fd-125">입력</span><span class="sxs-lookup"><span data-stu-id="315fd-125">INPUTS</span></span>

### <span data-ttu-id="315fd-126">System.String</span><span class="sxs-lookup"><span data-stu-id="315fd-126">System.String</span></span>

### <span data-ttu-id="315fd-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="315fd-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="315fd-128">출력</span><span class="sxs-lookup"><span data-stu-id="315fd-128">OUTPUTS</span></span>

### <span data-ttu-id="315fd-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="315fd-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="315fd-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="315fd-130">NOTES</span></span>

## <span data-ttu-id="315fd-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="315fd-131">RELATED LINKS</span></span>
