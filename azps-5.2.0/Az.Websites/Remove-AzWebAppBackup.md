---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: e50c711e730f3af79ce5d8825e6beeee9b663e00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326094"
---
# <span data-ttu-id="3ff48-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="3ff48-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="3ff48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ff48-102">SYNOPSIS</span></span>

## <span data-ttu-id="3ff48-103">구문</span><span class="sxs-lookup"><span data-stu-id="3ff48-103">SYNTAX</span></span>

### <span data-ttu-id="3ff48-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="3ff48-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff48-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="3ff48-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ff48-106">설명</span><span class="sxs-lookup"><span data-stu-id="3ff48-106">DESCRIPTION</span></span>
<span data-ttu-id="3ff48-107">**Remove-AzWebAppBackup** cmdlet은 Azure 웹앱의 지정된 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3ff48-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="3ff48-108">예제</span><span class="sxs-lookup"><span data-stu-id="3ff48-108">EXAMPLES</span></span>

### <span data-ttu-id="3ff48-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="3ff48-109">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="3ff48-110">이 명령은 리소스 그룹 Default-Web-WestUS에 속하는 WebAppStandard라는 웹앱에서 ID가 "12345"인 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3ff48-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="3ff48-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ff48-111">PARAMETERS</span></span>

### <span data-ttu-id="3ff48-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="3ff48-112">-BackupId</span></span>
<span data-ttu-id="3ff48-113">Backup Id</span><span class="sxs-lookup"><span data-stu-id="3ff48-113">Backup Id</span></span>

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

### <span data-ttu-id="3ff48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff48-114">-DefaultProfile</span></span>
<span data-ttu-id="3ff48-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ff48-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ff48-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3ff48-116">-Name</span></span>
<span data-ttu-id="3ff48-117">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="3ff48-117">WebApp Name</span></span>

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

### <span data-ttu-id="3ff48-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff48-118">-ResourceGroupName</span></span>
<span data-ttu-id="3ff48-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3ff48-119">Resource Group Name</span></span>

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

### <span data-ttu-id="3ff48-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="3ff48-120">-Slot</span></span>
<span data-ttu-id="3ff48-121">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="3ff48-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="3ff48-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3ff48-122">-WebApp</span></span>
<span data-ttu-id="3ff48-123">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="3ff48-123">WebApp Object</span></span>

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

### <span data-ttu-id="3ff48-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff48-124">CommonParameters</span></span>
<span data-ttu-id="3ff48-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3ff48-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff48-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3ff48-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff48-127">입력</span><span class="sxs-lookup"><span data-stu-id="3ff48-127">INPUTS</span></span>

### <span data-ttu-id="3ff48-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3ff48-128">System.String</span></span>

### <span data-ttu-id="3ff48-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="3ff48-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3ff48-130">출력</span><span class="sxs-lookup"><span data-stu-id="3ff48-130">OUTPUTS</span></span>

### <span data-ttu-id="3ff48-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span><span class="sxs-lookup"><span data-stu-id="3ff48-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="3ff48-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3ff48-132">NOTES</span></span>

## <span data-ttu-id="3ff48-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ff48-133">RELATED LINKS</span></span>
