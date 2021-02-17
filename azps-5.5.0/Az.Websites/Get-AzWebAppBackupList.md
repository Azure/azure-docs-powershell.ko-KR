---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 6ea805f1e3a3711c2efe6faefd73edf06c4b51fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198228"
---
# <span data-ttu-id="6f836-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="6f836-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="6f836-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f836-102">SYNOPSIS</span></span>

## <span data-ttu-id="6f836-103">구문</span><span class="sxs-lookup"><span data-stu-id="6f836-103">SYNTAX</span></span>

### <span data-ttu-id="6f836-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6f836-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f836-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6f836-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f836-106">설명</span><span class="sxs-lookup"><span data-stu-id="6f836-106">DESCRIPTION</span></span>
<span data-ttu-id="6f836-107">**Get-AzWebAppBackupList** cmdlet은 Azure 웹앱에 대한 백업 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6f836-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="6f836-108">예제</span><span class="sxs-lookup"><span data-stu-id="6f836-108">EXAMPLES</span></span>

### <span data-ttu-id="6f836-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="6f836-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="6f836-110">이 명령은 리소스 그룹 ContosoResourceGroup과 연결된 WebApp WebAppStandard와 관련된 백업 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6f836-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="6f836-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f836-111">PARAMETERS</span></span>

### <span data-ttu-id="6f836-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f836-112">-DefaultProfile</span></span>
<span data-ttu-id="6f836-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f836-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f836-114">-Name</span><span class="sxs-lookup"><span data-stu-id="6f836-114">-Name</span></span>
<span data-ttu-id="6f836-115">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="6f836-115">WebApp Name</span></span>

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

### <span data-ttu-id="6f836-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f836-116">-ResourceGroupName</span></span>
<span data-ttu-id="6f836-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6f836-117">Resource Group Name</span></span>

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

### <span data-ttu-id="6f836-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="6f836-118">-Slot</span></span>
<span data-ttu-id="6f836-119">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="6f836-119">Slot name</span></span>

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

### <span data-ttu-id="6f836-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6f836-120">-WebApp</span></span>
<span data-ttu-id="6f836-121">파이프된 WebApp</span><span class="sxs-lookup"><span data-stu-id="6f836-121">Piped WebApp</span></span>

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

### <span data-ttu-id="6f836-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f836-122">CommonParameters</span></span>
<span data-ttu-id="6f836-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f836-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f836-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6f836-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f836-125">입력</span><span class="sxs-lookup"><span data-stu-id="6f836-125">INPUTS</span></span>

### <span data-ttu-id="6f836-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6f836-126">System.String</span></span>

### <span data-ttu-id="6f836-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="6f836-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6f836-128">출력</span><span class="sxs-lookup"><span data-stu-id="6f836-128">OUTPUTS</span></span>

### <span data-ttu-id="6f836-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="6f836-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="6f836-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f836-130">NOTES</span></span>

## <span data-ttu-id="6f836-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f836-131">RELATED LINKS</span></span>
