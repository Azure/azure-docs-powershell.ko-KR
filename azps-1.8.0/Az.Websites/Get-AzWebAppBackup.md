---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: 30f1581ddd4668fbe4d4d4b6d8c902f6aac929ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698363"
---
# <span data-ttu-id="e0ef0-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e0ef0-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="e0ef0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0ef0-102">SYNOPSIS</span></span>

## <span data-ttu-id="e0ef0-103">구문과</span><span class="sxs-lookup"><span data-stu-id="e0ef0-103">SYNTAX</span></span>

### <span data-ttu-id="e0ef0-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e0ef0-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0ef0-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e0ef0-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0ef0-106">설명은</span><span class="sxs-lookup"><span data-stu-id="e0ef0-106">DESCRIPTION</span></span>
<span data-ttu-id="e0ef0-107">**AzWebAppBackup** cmdlet은 지정 된 Azure Web App 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0ef0-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="e0ef0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e0ef0-108">EXAMPLES</span></span>

### <span data-ttu-id="e0ef0-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="e0ef0-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="e0ef0-110">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 WebAppStandard 이라는 웹 앱에서 ID가 "12345" 인 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0ef0-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e0ef0-111">변수</span><span class="sxs-lookup"><span data-stu-id="e0ef0-111">PARAMETERS</span></span>

### <span data-ttu-id="e0ef0-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="e0ef0-112">-BackupId</span></span>
<span data-ttu-id="e0ef0-113">백업 Id</span><span class="sxs-lookup"><span data-stu-id="e0ef0-113">Backup Id</span></span>

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

### <span data-ttu-id="e0ef0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ef0-114">-DefaultProfile</span></span>
<span data-ttu-id="e0ef0-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0ef0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0ef0-116">-이름</span><span class="sxs-lookup"><span data-stu-id="e0ef0-116">-Name</span></span>
<span data-ttu-id="e0ef0-117">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="e0ef0-117">Webapp Name</span></span>

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

### <span data-ttu-id="e0ef0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ef0-118">-ResourceGroupName</span></span>
<span data-ttu-id="e0ef0-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e0ef0-119">Resource Group Name</span></span>

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

### <span data-ttu-id="e0ef0-120">-슬롯</span><span class="sxs-lookup"><span data-stu-id="e0ef0-120">-Slot</span></span>
<span data-ttu-id="e0ef0-121">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="e0ef0-121">Slot Name</span></span>

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

### <span data-ttu-id="e0ef0-122">-Web app</span><span class="sxs-lookup"><span data-stu-id="e0ef0-122">-WebApp</span></span>
<span data-ttu-id="e0ef0-123">파이프 Web app</span><span class="sxs-lookup"><span data-stu-id="e0ef0-123">Piped WebApp</span></span>

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

### <span data-ttu-id="e0ef0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ef0-124">CommonParameters</span></span>
<span data-ttu-id="e0ef0-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0ef0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ef0-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0ef0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ef0-127">입력</span><span class="sxs-lookup"><span data-stu-id="e0ef0-127">INPUTS</span></span>

### <span data-ttu-id="e0ef0-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e0ef0-128">System.String</span></span>

### <span data-ttu-id="e0ef0-129">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="e0ef0-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e0ef0-130">출력</span><span class="sxs-lookup"><span data-stu-id="e0ef0-130">OUTPUTS</span></span>

### <span data-ttu-id="e0ef0-131">AzureWebAppBackup (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="e0ef0-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="e0ef0-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e0ef0-132">NOTES</span></span>

## <span data-ttu-id="e0ef0-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0ef0-133">RELATED LINKS</span></span>
