---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 480532e2fffcc2b03a57c7d0a63cc2737844f652
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034195"
---
# <span data-ttu-id="9f577-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="9f577-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="9f577-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f577-102">SYNOPSIS</span></span>

## <span data-ttu-id="9f577-103">구문과</span><span class="sxs-lookup"><span data-stu-id="9f577-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f577-104">설명은</span><span class="sxs-lookup"><span data-stu-id="9f577-104">DESCRIPTION</span></span>
<span data-ttu-id="9f577-105">**AzWebAppDatabaseBackupSetting** cmdlet은 새 Azure Web App 백업 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="9f577-106">예제의</span><span class="sxs-lookup"><span data-stu-id="9f577-106">EXAMPLES</span></span>

### <span data-ttu-id="9f577-107">raid-1</span><span class="sxs-lookup"><span data-stu-id="9f577-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="9f577-108">리소스 그룹 기본값-웹 WestUS에 있는 지정 된 앱 ContosoWebApp에 대 한 SqlAzure 유형의 데이터베이스 백업 설정 (연결 문자열)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9f577-109">변수</span><span class="sxs-lookup"><span data-stu-id="9f577-109">PARAMETERS</span></span>

### <span data-ttu-id="9f577-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="9f577-110">-ConnectionString</span></span>
<span data-ttu-id="9f577-111">연결 문자열</span><span class="sxs-lookup"><span data-stu-id="9f577-111">Connection String</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f577-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="9f577-112">-ConnectionStringName</span></span>
<span data-ttu-id="9f577-113">연결 문자열 이름</span><span class="sxs-lookup"><span data-stu-id="9f577-113">Connection String Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f577-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="9f577-114">-DatabaseType</span></span>
<span data-ttu-id="9f577-115">데이터베이스 형식 (예: "SqlAzure" 또는 "MySql")</span><span class="sxs-lookup"><span data-stu-id="9f577-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f577-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f577-116">-DefaultProfile</span></span>
<span data-ttu-id="9f577-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f577-118">-이름</span><span class="sxs-lookup"><span data-stu-id="9f577-118">-Name</span></span>
<span data-ttu-id="9f577-119">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="9f577-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f577-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f577-120">CommonParameters</span></span>
<span data-ttu-id="9f577-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f577-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f577-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f577-123">입력</span><span class="sxs-lookup"><span data-stu-id="9f577-123">INPUTS</span></span>

### <span data-ttu-id="9f577-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9f577-124">System.String</span></span>

## <span data-ttu-id="9f577-125">출력</span><span class="sxs-lookup"><span data-stu-id="9f577-125">OUTPUTS</span></span>

### <span data-ttu-id="9f577-126">DatabaseBackupSetting/. m i.</span><span class="sxs-lookup"><span data-stu-id="9f577-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="9f577-127">상속자</span><span class="sxs-lookup"><span data-stu-id="9f577-127">NOTES</span></span>

## <span data-ttu-id="9f577-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f577-128">RELATED LINKS</span></span>
