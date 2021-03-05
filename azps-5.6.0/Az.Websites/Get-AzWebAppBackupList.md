---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: f70caa984fde48db6b2d1d147ebf62f544f2ed9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972379"
---
# <span data-ttu-id="7f783-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="7f783-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="7f783-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f783-102">SYNOPSIS</span></span>

## <span data-ttu-id="7f783-103">구문</span><span class="sxs-lookup"><span data-stu-id="7f783-103">SYNTAX</span></span>

### <span data-ttu-id="7f783-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="7f783-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f783-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="7f783-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f783-106">설명</span><span class="sxs-lookup"><span data-stu-id="7f783-106">DESCRIPTION</span></span>
<span data-ttu-id="7f783-107">**Get-AzWebAppBackupList** cmdlet은 Azure Web App에 대한 백업 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7f783-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="7f783-108">예제</span><span class="sxs-lookup"><span data-stu-id="7f783-108">EXAMPLES</span></span>

### <span data-ttu-id="7f783-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f783-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="7f783-110">이 명령은 리소스 그룹 ContosoResourceGroup과 연결된 WebApp WebAppStandard와 관련된 백업 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7f783-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="7f783-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7f783-111">PARAMETERS</span></span>

### <span data-ttu-id="7f783-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f783-112">-DefaultProfile</span></span>
<span data-ttu-id="7f783-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f783-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f783-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7f783-114">-Name</span></span>
<span data-ttu-id="7f783-115">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="7f783-115">WebApp Name</span></span>

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

### <span data-ttu-id="7f783-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f783-116">-ResourceGroupName</span></span>
<span data-ttu-id="7f783-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7f783-117">Resource Group Name</span></span>

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

### <span data-ttu-id="7f783-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="7f783-118">-Slot</span></span>
<span data-ttu-id="7f783-119">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="7f783-119">Slot name</span></span>

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

### <span data-ttu-id="7f783-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7f783-120">-WebApp</span></span>
<span data-ttu-id="7f783-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="7f783-121">Piped WebApp</span></span>

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

### <span data-ttu-id="7f783-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f783-122">CommonParameters</span></span>
<span data-ttu-id="7f783-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f783-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f783-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7f783-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f783-125">입력</span><span class="sxs-lookup"><span data-stu-id="7f783-125">INPUTS</span></span>

### <span data-ttu-id="7f783-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7f783-126">System.String</span></span>

### <span data-ttu-id="7f783-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="7f783-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7f783-128">출력</span><span class="sxs-lookup"><span data-stu-id="7f783-128">OUTPUTS</span></span>

### <span data-ttu-id="7f783-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="7f783-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="7f783-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f783-130">NOTES</span></span>

## <span data-ttu-id="7f783-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f783-131">RELATED LINKS</span></span>
