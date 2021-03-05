---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: 70dea111b2fc48e2d5063db21dd53a6e9ca76f75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983803"
---
# <span data-ttu-id="954f3-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="954f3-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="954f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="954f3-102">SYNOPSIS</span></span>

## <span data-ttu-id="954f3-103">구문</span><span class="sxs-lookup"><span data-stu-id="954f3-103">SYNTAX</span></span>

### <span data-ttu-id="954f3-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="954f3-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="954f3-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="954f3-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="954f3-106">설명</span><span class="sxs-lookup"><span data-stu-id="954f3-106">DESCRIPTION</span></span>
<span data-ttu-id="954f3-107">**Get-AzWebAppBackup** cmdlet은 Azure Web App의 지정된 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="954f3-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="954f3-108">예제</span><span class="sxs-lookup"><span data-stu-id="954f3-108">EXAMPLES</span></span>

### <span data-ttu-id="954f3-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="954f3-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="954f3-110">이 명령은 리소스 그룹 Default-Web-WestUS에 속하는 WebAppStandard라는 웹앱에서 ID "12345"를 사용하여 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="954f3-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="954f3-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="954f3-111">PARAMETERS</span></span>

### <span data-ttu-id="954f3-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="954f3-112">-BackupId</span></span>
<span data-ttu-id="954f3-113">백업 ID</span><span class="sxs-lookup"><span data-stu-id="954f3-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="954f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="954f3-114">-DefaultProfile</span></span>
<span data-ttu-id="954f3-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="954f3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="954f3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="954f3-116">-Name</span></span>
<span data-ttu-id="954f3-117">웹앱 이름</span><span class="sxs-lookup"><span data-stu-id="954f3-117">Webapp Name</span></span>

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

### <span data-ttu-id="954f3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="954f3-118">-ResourceGroupName</span></span>
<span data-ttu-id="954f3-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="954f3-119">Resource Group Name</span></span>

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

### <span data-ttu-id="954f3-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="954f3-120">-Slot</span></span>
<span data-ttu-id="954f3-121">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="954f3-121">Slot Name</span></span>

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

### <span data-ttu-id="954f3-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="954f3-122">-WebApp</span></span>
<span data-ttu-id="954f3-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="954f3-123">Piped WebApp</span></span>

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

### <span data-ttu-id="954f3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="954f3-124">CommonParameters</span></span>
<span data-ttu-id="954f3-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="954f3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="954f3-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="954f3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="954f3-127">입력</span><span class="sxs-lookup"><span data-stu-id="954f3-127">INPUTS</span></span>

### <span data-ttu-id="954f3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="954f3-128">System.String</span></span>

### <span data-ttu-id="954f3-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="954f3-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="954f3-130">출력</span><span class="sxs-lookup"><span data-stu-id="954f3-130">OUTPUTS</span></span>

### <span data-ttu-id="954f3-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="954f3-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="954f3-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="954f3-132">NOTES</span></span>

## <span data-ttu-id="954f3-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="954f3-133">RELATED LINKS</span></span>
