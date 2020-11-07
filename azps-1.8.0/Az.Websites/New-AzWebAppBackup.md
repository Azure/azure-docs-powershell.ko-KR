---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: 2ef015c3f793dd4636632f17568feb9aaf1b5ad2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698333"
---
# <span data-ttu-id="b809e-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="b809e-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="b809e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b809e-102">SYNOPSIS</span></span>

## <span data-ttu-id="b809e-103">구문과</span><span class="sxs-lookup"><span data-stu-id="b809e-103">SYNTAX</span></span>

### <span data-ttu-id="b809e-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b809e-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="b809e-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b809e-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="b809e-106">설명은</span><span class="sxs-lookup"><span data-stu-id="b809e-106">DESCRIPTION</span></span>
<span data-ttu-id="b809e-107">**AzWebAppBackup** Cmdlet은 Azure Web App 백업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b809e-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="b809e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b809e-108">EXAMPLES</span></span>

### <span data-ttu-id="b809e-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="b809e-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="b809e-110">리소스 그룹 기본값-웹-WestUS에 있는 지정 된 앱 ContosoWebApp의 백업을 만듭니다. https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="b809e-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="b809e-111">변수</span><span class="sxs-lookup"><span data-stu-id="b809e-111">PARAMETERS</span></span>

### <span data-ttu-id="b809e-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="b809e-112">-BackupName</span></span>
<span data-ttu-id="b809e-113">백업 이름</span><span class="sxs-lookup"><span data-stu-id="b809e-113">Backup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b809e-114">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="b809e-114">-Databases</span></span>
<span data-ttu-id="b809e-115">DatabaseBackupSetting 유형의 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="b809e-115">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b809e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b809e-116">-DefaultProfile</span></span>
<span data-ttu-id="b809e-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b809e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b809e-118">-이름</span><span class="sxs-lookup"><span data-stu-id="b809e-118">-Name</span></span>
<span data-ttu-id="b809e-119">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="b809e-119">WebApp Name</span></span>

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

### <span data-ttu-id="b809e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b809e-120">-ResourceGroupName</span></span>
<span data-ttu-id="b809e-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b809e-121">Resource Group Name</span></span>

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

### <span data-ttu-id="b809e-122">-슬롯</span><span class="sxs-lookup"><span data-stu-id="b809e-122">-Slot</span></span>
<span data-ttu-id="b809e-123">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="b809e-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b809e-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="b809e-124">-StorageAccountUrl</span></span>
<span data-ttu-id="b809e-125">저장소 계정 Url</span><span class="sxs-lookup"><span data-stu-id="b809e-125">Storage Account Url</span></span>

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

### <span data-ttu-id="b809e-126">-Web app</span><span class="sxs-lookup"><span data-stu-id="b809e-126">-WebApp</span></span>
<span data-ttu-id="b809e-127">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="b809e-127">WebApp Object</span></span>

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

### <span data-ttu-id="b809e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b809e-128">CommonParameters</span></span>
<span data-ttu-id="b809e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b809e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b809e-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b809e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b809e-131">입력</span><span class="sxs-lookup"><span data-stu-id="b809e-131">INPUTS</span></span>

### <span data-ttu-id="b809e-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b809e-132">System.String</span></span>

### <span data-ttu-id="b809e-133">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="b809e-133">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="b809e-134">DatabaseBackupSetting [] (으)로</span><span class="sxs-lookup"><span data-stu-id="b809e-134">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="b809e-135">출력</span><span class="sxs-lookup"><span data-stu-id="b809e-135">OUTPUTS</span></span>

### <span data-ttu-id="b809e-136">AzureWebAppBackup (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="b809e-136">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="b809e-137">상속자</span><span class="sxs-lookup"><span data-stu-id="b809e-137">NOTES</span></span>

## <span data-ttu-id="b809e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b809e-138">RELATED LINKS</span></span>
