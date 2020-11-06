---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 7eea25d4b82dc8a424fea0cbd3e361014c77c396
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532555"
---
# <span data-ttu-id="9a71b-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="9a71b-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="9a71b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a71b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a71b-103">구문과</span><span class="sxs-lookup"><span data-stu-id="9a71b-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a71b-104">설명은</span><span class="sxs-lookup"><span data-stu-id="9a71b-104">DESCRIPTION</span></span>
<span data-ttu-id="9a71b-105">**AzureRmWebAppDatabaseBackupSetting** cmdlet은 새 Azure Web App 백업 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a71b-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="9a71b-106">예제의</span><span class="sxs-lookup"><span data-stu-id="9a71b-106">EXAMPLES</span></span>

### <span data-ttu-id="9a71b-107">raid-1</span><span class="sxs-lookup"><span data-stu-id="9a71b-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="9a71b-108">리소스 그룹 기본값-웹 WestUS에 있는 지정 된 앱 ContosoWebApp에 대 한 SqlAzure 유형의 데이터베이스 백업 설정 (연결 문자열)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a71b-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9a71b-109">변수</span><span class="sxs-lookup"><span data-stu-id="9a71b-109">PARAMETERS</span></span>

### <span data-ttu-id="9a71b-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="9a71b-110">-ConnectionString</span></span>
<span data-ttu-id="9a71b-111">연결 문자열</span><span class="sxs-lookup"><span data-stu-id="9a71b-111">Connection String</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71b-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="9a71b-112">-ConnectionStringName</span></span>
<span data-ttu-id="9a71b-113">연결 문자열 이름</span><span class="sxs-lookup"><span data-stu-id="9a71b-113">Connection String Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71b-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="9a71b-114">-DatabaseType</span></span>
<span data-ttu-id="9a71b-115">데이터베이스 형식 (예: "SqlAzure" 또는 "MySql")</span><span class="sxs-lookup"><span data-stu-id="9a71b-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a71b-116">-DefaultProfile</span></span>
<span data-ttu-id="9a71b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a71b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a71b-118">-이름</span><span class="sxs-lookup"><span data-stu-id="9a71b-118">-Name</span></span>
<span data-ttu-id="9a71b-119">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="9a71b-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a71b-120">CommonParameters</span></span>
<span data-ttu-id="9a71b-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a71b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a71b-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a71b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a71b-123">입력</span><span class="sxs-lookup"><span data-stu-id="9a71b-123">INPUTS</span></span>

### <span data-ttu-id="9a71b-124">않아야</span><span class="sxs-lookup"><span data-stu-id="9a71b-124">None</span></span>
<span data-ttu-id="9a71b-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a71b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a71b-126">출력</span><span class="sxs-lookup"><span data-stu-id="9a71b-126">OUTPUTS</span></span>

### <span data-ttu-id="9a71b-127">DatabaseBackupSetting/. m i.</span><span class="sxs-lookup"><span data-stu-id="9a71b-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="9a71b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="9a71b-128">NOTES</span></span>

## <span data-ttu-id="9a71b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a71b-129">RELATED LINKS</span></span>

