---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationconnectioninfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: aca970403d7ef85733d808c8e21df3d0b2066f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528151"
---
# <span data-ttu-id="2f80d-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="2f80d-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="2f80d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f80d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f80d-103">연결에 대 한 서버 유형 및 이름을 지정 하는 새 연결 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f80d-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f80d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2f80d-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="2f80d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2f80d-105">DESCRIPTION</span></span>
<span data-ttu-id="2f80d-106">New-AzureRmDataMigrationConnectionInfo cmdlet은 연결에 대 한 서버 유형을 지정 하는 새 연결 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f80d-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 



## <span data-ttu-id="2f80d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2f80d-107">EXAMPLES</span></span>

### <span data-ttu-id="2f80d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2f80d-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```
<span data-ttu-id="2f80d-109">앞의 예제에서는 ServerType 매개 변수로 SQL을 제공 하는 새 연결 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f80d-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>


## <span data-ttu-id="2f80d-110">변수</span><span class="sxs-lookup"><span data-stu-id="2f80d-110">PARAMETERS</span></span>

### <span data-ttu-id="2f80d-111">-확인</span><span class="sxs-lookup"><span data-stu-id="2f80d-111">-Confirm</span></span>
<span data-ttu-id="2f80d-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f80d-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="2f80d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f80d-113">-DefaultProfile</span></span>
<span data-ttu-id="2f80d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f80d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f80d-115">-ServerType</span><span class="sxs-lookup"><span data-stu-id="2f80d-115">-ServerType</span></span>
<span data-ttu-id="2f80d-116">연결할 서버 유형을 설명 하는 열거형입니다.</span><span class="sxs-lookup"><span data-stu-id="2f80d-116">Enum that describes server type to connect to.</span></span> <span data-ttu-id="2f80d-117">현재 지원 되는 값은 sql Server 및 SQLDB for SQL Azure 데이터베이스용 SQL입니다.</span><span class="sxs-lookup"><span data-stu-id="2f80d-117">Currently supported values are SQL for SQL Server and SQLDB for SQL Azure Database.</span></span> 

```yaml
Type: ServerTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL, SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="2f80d-118">-AuthType</span><span class="sxs-lookup"><span data-stu-id="2f80d-118">-AuthType</span></span>
<span data-ttu-id="2f80d-119">연결에 사용할 인증 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2f80d-119">Authentication type to use for connection.</span></span> <span data-ttu-id="2f80d-120">사용할 수 있는 값은 SqlAuthentication 및 WindowsAuthentication입니다.</span><span class="sxs-lookup"><span data-stu-id="2f80d-120">Possible values are SqlAuthentication and WindowsAuthentication</span></span>

```yaml
Type: AuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f80d-121">-DataSource</span><span class="sxs-lookup"><span data-stu-id="2f80d-121">-DataSource</span></span>
<span data-ttu-id="2f80d-122">서버 연결 \ n 연결할 \ \ 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f80d-122">Server address\name to connect to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f80d-123">-TrustServerCertificate</span><span class="sxs-lookup"><span data-stu-id="2f80d-123">-TrustServerCertificate</span></span>
<span data-ttu-id="2f80d-124">암호화가 발생 하는 것을 보장 하는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="2f80d-124">Boolean indicating to guarantee that encryption takes place.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f80d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f80d-125">-WhatIf</span></span>
<span data-ttu-id="2f80d-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2f80d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f80d-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f80d-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```





## <span data-ttu-id="2f80d-128">입력</span><span class="sxs-lookup"><span data-stu-id="2f80d-128">INPUTS</span></span>

### <span data-ttu-id="2f80d-129">않아야</span><span class="sxs-lookup"><span data-stu-id="2f80d-129">None</span></span>


## <span data-ttu-id="2f80d-130">출력</span><span class="sxs-lookup"><span data-stu-id="2f80d-130">OUTPUTS</span></span>

### <span data-ttu-id="2f80d-131">DataMigration. ConnectionInfo/.</span><span class="sxs-lookup"><span data-stu-id="2f80d-131">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>


## <span data-ttu-id="2f80d-132">상속자</span><span class="sxs-lookup"><span data-stu-id="2f80d-132">NOTES</span></span>

## <span data-ttu-id="2f80d-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f80d-133">RELATED LINKS</span></span>

