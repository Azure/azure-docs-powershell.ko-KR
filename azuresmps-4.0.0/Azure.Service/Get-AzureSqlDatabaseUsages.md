---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 9953AF91-2424-4BD1-9133-E0E07AC1087E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a17ff5e4ec976fcf0c6be02e3fbc373d7ffd2f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046563"
---
# <span data-ttu-id="4eebd-101">Get-AzureSqlDatabaseUsages</span><span class="sxs-lookup"><span data-stu-id="4eebd-101">Get-AzureSqlDatabaseUsages</span></span>

## <span data-ttu-id="4eebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eebd-102">SYNOPSIS</span></span>
<span data-ttu-id="4eebd-103">SQL 데이터베이스의 크기 및 크기 제한을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4eebd-103">Gets the size and size limit of a SQL Database.</span></span>

## <span data-ttu-id="4eebd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4eebd-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseUsages -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4eebd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4eebd-105">DESCRIPTION</span></span>
<span data-ttu-id="4eebd-106">**AzureSqlDatabaseUsages** Cmdlet은 Azure SQL 데이터베이스의 현재 크기 및 크기 제한을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4eebd-106">The **Get-AzureSqlDatabaseUsages** cmdlet gets the current size and size limit of an Azure SQL Database.</span></span>

## <span data-ttu-id="4eebd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4eebd-107">EXAMPLES</span></span>

### <span data-ttu-id="4eebd-108">예제 1: SQL 데이터베이스에 대 한 사용 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="4eebd-108">Example 1: Get usage information for a SQL Database</span></span>
```
PS C:\> Get-AzureSqlDatabaseUsages -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="4eebd-109">이 명령은 Server01에 Database01 이라는 SQL 데이터베이스에 대 한 크기 및 크기 제한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4eebd-109">This command gets the size and size limit information for the SQL Database named Database01 on Server01.</span></span>

## <span data-ttu-id="4eebd-110">변수</span><span class="sxs-lookup"><span data-stu-id="4eebd-110">PARAMETERS</span></span>

### <span data-ttu-id="4eebd-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4eebd-111">-DatabaseName</span></span>
<span data-ttu-id="4eebd-112">Azure SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eebd-112">Specifies the name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="4eebd-113">-Profile</span></span>
<span data-ttu-id="4eebd-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eebd-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4eebd-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4eebd-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4eebd-116">-ServerName</span></span>
<span data-ttu-id="4eebd-117">Azure SQL 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eebd-117">Specifies the name of the server that hosts the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eebd-118">CommonParameters</span></span>
<span data-ttu-id="4eebd-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eebd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eebd-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eebd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eebd-121">입력</span><span class="sxs-lookup"><span data-stu-id="4eebd-121">INPUTS</span></span>

## <span data-ttu-id="4eebd-122">출력</span><span class="sxs-lookup"><span data-stu-id="4eebd-122">OUTPUTS</span></span>

## <span data-ttu-id="4eebd-123">상속자</span><span class="sxs-lookup"><span data-stu-id="4eebd-123">NOTES</span></span>

## <span data-ttu-id="4eebd-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4eebd-124">RELATED LINKS</span></span>

