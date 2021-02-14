---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: e8c3f7543062613527e7f52be2cd6493f53c5f60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188716"
---
# <span data-ttu-id="4d34d-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="4d34d-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="4d34d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d34d-102">SYNOPSIS</span></span>

## <span data-ttu-id="4d34d-103">구문</span><span class="sxs-lookup"><span data-stu-id="4d34d-103">SYNTAX</span></span>

### <span data-ttu-id="4d34d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="4d34d-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d34d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="4d34d-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d34d-106">설명</span><span class="sxs-lookup"><span data-stu-id="4d34d-106">DESCRIPTION</span></span>
<span data-ttu-id="4d34d-107">**Get-AzWebAppBackup** cmdlet은 Azure 웹앱의 지정된 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d34d-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="4d34d-108">예제</span><span class="sxs-lookup"><span data-stu-id="4d34d-108">EXAMPLES</span></span>

### <span data-ttu-id="4d34d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="4d34d-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="4d34d-110">이 명령은 리소스 그룹 Default-Web-WestUS에 속하는 WebAppStandard라는 웹앱에서 ID가 "12345"인 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d34d-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="4d34d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d34d-111">PARAMETERS</span></span>

### <span data-ttu-id="4d34d-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="4d34d-112">-BackupId</span></span>
<span data-ttu-id="4d34d-113">Backup Id</span><span class="sxs-lookup"><span data-stu-id="4d34d-113">Backup Id</span></span>

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

### <span data-ttu-id="4d34d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d34d-114">-DefaultProfile</span></span>
<span data-ttu-id="4d34d-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d34d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d34d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4d34d-116">-Name</span></span>
<span data-ttu-id="4d34d-117">웹앱 이름</span><span class="sxs-lookup"><span data-stu-id="4d34d-117">Webapp Name</span></span>

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

### <span data-ttu-id="4d34d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d34d-118">-ResourceGroupName</span></span>
<span data-ttu-id="4d34d-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4d34d-119">Resource Group Name</span></span>

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

### <span data-ttu-id="4d34d-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="4d34d-120">-Slot</span></span>
<span data-ttu-id="4d34d-121">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="4d34d-121">Slot Name</span></span>

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

### <span data-ttu-id="4d34d-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4d34d-122">-WebApp</span></span>
<span data-ttu-id="4d34d-123">파이프된 WebApp</span><span class="sxs-lookup"><span data-stu-id="4d34d-123">Piped WebApp</span></span>

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

### <span data-ttu-id="4d34d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d34d-124">CommonParameters</span></span>
<span data-ttu-id="4d34d-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d34d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d34d-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4d34d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d34d-127">입력</span><span class="sxs-lookup"><span data-stu-id="4d34d-127">INPUTS</span></span>

### <span data-ttu-id="4d34d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4d34d-128">System.String</span></span>

### <span data-ttu-id="4d34d-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="4d34d-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4d34d-130">출력</span><span class="sxs-lookup"><span data-stu-id="4d34d-130">OUTPUTS</span></span>

### <span data-ttu-id="4d34d-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="4d34d-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="4d34d-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d34d-132">NOTES</span></span>

## <span data-ttu-id="4d34d-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d34d-133">RELATED LINKS</span></span>
