---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208869"
---
# <span data-ttu-id="fa3d7-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="fa3d7-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="fa3d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa3d7-102">SYNOPSIS</span></span>
<span data-ttu-id="fa3d7-103">웹앱에 사용할 수 있는 스냅숏을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="fa3d7-104">구문</span><span class="sxs-lookup"><span data-stu-id="fa3d7-104">SYNTAX</span></span>

### <span data-ttu-id="fa3d7-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="fa3d7-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa3d7-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="fa3d7-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa3d7-107">설명</span><span class="sxs-lookup"><span data-stu-id="fa3d7-107">DESCRIPTION</span></span>
<span data-ttu-id="fa3d7-108">**Get-AzWebAppSnapshot** cmdlet은 웹앱에 대한 모든 스냅숏을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="fa3d7-109">스냅숏은 웹앱의 파일 및 설정에 대한 자동 백업입니다.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="fa3d7-110">**Restore-AzWebAppSnapshot** cmdlet을 사용하여 스냅숏을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="fa3d7-111">예제</span><span class="sxs-lookup"><span data-stu-id="fa3d7-111">EXAMPLES</span></span>

### <span data-ttu-id="fa3d7-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="fa3d7-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="fa3d7-113">"Default-Web-WestUS" 리소스 그룹에 "스테이징"이라는 슬롯이 있는 "ContosoApp"이라는 웹앱에 대한 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="fa3d7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa3d7-114">PARAMETERS</span></span>

### <span data-ttu-id="fa3d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa3d7-115">-DefaultProfile</span></span>
<span data-ttu-id="fa3d7-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa3d7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fa3d7-117">-Name</span></span>
<span data-ttu-id="fa3d7-118">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-118">The name of the web app.</span></span>

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

### <span data-ttu-id="fa3d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa3d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="fa3d7-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="fa3d7-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="fa3d7-121">-Slot</span></span>
<span data-ttu-id="fa3d7-122">웹앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="fa3d7-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="fa3d7-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="fa3d7-124">보조 배율 단위에서 스냅숏을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-124">Read the snapshots from a secondary scale unit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa3d7-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fa3d7-125">-WebApp</span></span>
<span data-ttu-id="fa3d7-126">웹앱 개체</span><span class="sxs-lookup"><span data-stu-id="fa3d7-126">The web app object</span></span>

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

### <span data-ttu-id="fa3d7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa3d7-127">CommonParameters</span></span>
<span data-ttu-id="fa3d7-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa3d7-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa3d7-130">입력</span><span class="sxs-lookup"><span data-stu-id="fa3d7-130">INPUTS</span></span>

### <span data-ttu-id="fa3d7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fa3d7-131">System.String</span></span>

### <span data-ttu-id="fa3d7-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="fa3d7-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fa3d7-133">출력</span><span class="sxs-lookup"><span data-stu-id="fa3d7-133">OUTPUTS</span></span>

### <span data-ttu-id="fa3d7-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="fa3d7-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="fa3d7-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fa3d7-135">NOTES</span></span>

## <span data-ttu-id="fa3d7-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa3d7-136">RELATED LINKS</span></span>
