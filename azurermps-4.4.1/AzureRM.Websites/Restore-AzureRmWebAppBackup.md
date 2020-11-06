---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: 07cf4daffeaf00c516bc5b179e5f4a2133a2c4ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525447"
---
# <span data-ttu-id="0bcf0-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="0bcf0-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="0bcf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bcf0-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bcf0-103">구문과</span><span class="sxs-lookup"><span data-stu-id="0bcf0-103">SYNTAX</span></span>

### <span data-ttu-id="0bcf0-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="0bcf0-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="0bcf0-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="0bcf0-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="0bcf0-106">설명은</span><span class="sxs-lookup"><span data-stu-id="0bcf0-106">DESCRIPTION</span></span>
<span data-ttu-id="0bcf0-107">**Restore-AzureRmWebAppBackup** Cmdlet은 Azure Web App 백업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bcf0-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="0bcf0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0bcf0-108">EXAMPLES</span></span>

### <span data-ttu-id="0bcf0-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="0bcf0-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="0bcf0-110">리소스 그룹 Default-WestUS 내에 있는 지정 된 앱 ContosoWebApp의 백업을 다음 위치의 blob "myBlob"에 복원 합니다. https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="0bcf0-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="0bcf0-111">변수</span><span class="sxs-lookup"><span data-stu-id="0bcf0-111">PARAMETERS</span></span>

### <span data-ttu-id="0bcf0-112">-BlobName</span><span class="sxs-lookup"><span data-stu-id="0bcf0-112">-BlobName</span></span>
<span data-ttu-id="0bcf0-113">Blob 이름</span><span class="sxs-lookup"><span data-stu-id="0bcf0-113">Blob Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bcf0-114">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="0bcf0-114">-Databases</span></span>
<span data-ttu-id="0bcf0-115">DatabaseBackupSetting 유형의 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="0bcf0-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="0bcf0-116">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="0bcf0-116">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="0bcf0-117">충돌 하는 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="0bcf0-117">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bcf0-118">-이름</span><span class="sxs-lookup"><span data-stu-id="0bcf0-118">-Name</span></span>
<span data-ttu-id="0bcf0-119">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="0bcf0-119">WebApp Name</span></span>

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

### <span data-ttu-id="0bcf0-120">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="0bcf0-120">-Overwrite</span></span>
<span data-ttu-id="0bcf0-121">덮어쓰기 옵션</span><span class="sxs-lookup"><span data-stu-id="0bcf0-121">Overwrite Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bcf0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bcf0-122">-ResourceGroupName</span></span>
<span data-ttu-id="0bcf0-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0bcf0-123">Resource Group Name</span></span>

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

### <span data-ttu-id="0bcf0-124">-슬롯</span><span class="sxs-lookup"><span data-stu-id="0bcf0-124">-Slot</span></span>
<span data-ttu-id="0bcf0-125">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="0bcf0-125">WebApp Slot Name</span></span>

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

### <span data-ttu-id="0bcf0-126">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="0bcf0-126">-StorageAccountUrl</span></span>
<span data-ttu-id="0bcf0-127">저장소 계정 Url</span><span class="sxs-lookup"><span data-stu-id="0bcf0-127">Storage Account Url</span></span>

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

### <span data-ttu-id="0bcf0-128">-Web app</span><span class="sxs-lookup"><span data-stu-id="0bcf0-128">-WebApp</span></span>
<span data-ttu-id="0bcf0-129">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="0bcf0-129">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bcf0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bcf0-130">-DefaultProfile</span></span>
<span data-ttu-id="0bcf0-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0bcf0-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bcf0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bcf0-132">CommonParameters</span></span>
<span data-ttu-id="0bcf0-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bcf0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bcf0-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bcf0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bcf0-135">입력</span><span class="sxs-lookup"><span data-stu-id="0bcf0-135">INPUTS</span></span>

### <span data-ttu-id="0bcf0-136">Site</span><span class="sxs-lookup"><span data-stu-id="0bcf0-136">Site</span></span>
<span data-ttu-id="0bcf0-137">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bcf0-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0bcf0-138">출력</span><span class="sxs-lookup"><span data-stu-id="0bcf0-138">OUTPUTS</span></span>

## <span data-ttu-id="0bcf0-139">상속자</span><span class="sxs-lookup"><span data-stu-id="0bcf0-139">NOTES</span></span>

## <span data-ttu-id="0bcf0-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0bcf0-140">RELATED LINKS</span></span>

