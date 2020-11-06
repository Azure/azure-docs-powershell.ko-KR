---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C0BE6C8D-37F5-445F-AE15-2CD4F8D8E031
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: e36030cbe1ccfe78db625d9d4142de13ba2f54ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527631"
---
# <span data-ttu-id="0545c-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="0545c-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="0545c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0545c-102">SYNOPSIS</span></span>
<span data-ttu-id="0545c-103">Data Lake Analytics 카탈로그 비밀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0545c-103">Creates a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0545c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0545c-104">SYNTAX</span></span>

### <span data-ttu-id="0545c-105">전체 URI 지정</span><span class="sxs-lookup"><span data-stu-id="0545c-105">Specify full URI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0545c-106">호스트 이름 및 포트 지정</span><span class="sxs-lookup"><span data-stu-id="0545c-106">Specify host name and port</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0545c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0545c-107">DESCRIPTION</span></span>
<span data-ttu-id="0545c-108">**AzureRmDataLakeAnalyticsCatalogSecret** Cmdlet은 Azure Data Lake Analytics 카탈로그에서 사용할 비밀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0545c-108">The **New-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet creates a secret to use in an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="0545c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0545c-109">EXAMPLES</span></span>

### <span data-ttu-id="0545c-110">예제 1: 카탈로그에 대 한 비밀 가져오기</span><span class="sxs-lookup"><span data-stu-id="0545c-110">Example 1: Get the secret for a catalog</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="0545c-111">이 명령은 지정 된 계정, 데이터베이스, 자격 증명 및 호스트에 해당 하는 암호를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0545c-111">This command gets the secret corresponding to the specified account, database, credential, and host.</span></span>

## <span data-ttu-id="0545c-112">변수</span><span class="sxs-lookup"><span data-stu-id="0545c-112">PARAMETERS</span></span>

### <span data-ttu-id="0545c-113">-계정</span><span class="sxs-lookup"><span data-stu-id="0545c-113">-Account</span></span>
<span data-ttu-id="0545c-114">Data Lake Analytics 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0545c-114">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0545c-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="0545c-115">-DatabaseHost</span></span>
<span data-ttu-id="0545c-116">비밀이 연결 되는 데이터베이스의 호스트 이름을 ' mydatabase.contoso.com ' 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0545c-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0545c-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0545c-117">-DatabaseName</span></span>
<span data-ttu-id="0545c-118">비밀을 저장 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0545c-118">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="0545c-119">-포트</span><span class="sxs-lookup"><span data-stu-id="0545c-119">-Port</span></span>
<span data-ttu-id="0545c-120">비밀의 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0545c-120">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0545c-121">-비밀</span><span class="sxs-lookup"><span data-stu-id="0545c-121">-Secret</span></span>
<span data-ttu-id="0545c-122">비밀의 이름과 비밀 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0545c-122">Specifies the name and password of the secret.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0545c-123">-Uri</span><span class="sxs-lookup"><span data-stu-id="0545c-123">-Uri</span></span>
<span data-ttu-id="0545c-124">비밀의 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0545c-124">Specifies the Uniform Resource Identifier (URI) of the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0545c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0545c-125">-DefaultProfile</span></span>
<span data-ttu-id="0545c-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0545c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0545c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0545c-127">CommonParameters</span></span>
<span data-ttu-id="0545c-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0545c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0545c-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0545c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0545c-130">입력</span><span class="sxs-lookup"><span data-stu-id="0545c-130">INPUTS</span></span>

## <span data-ttu-id="0545c-131">출력</span><span class="sxs-lookup"><span data-stu-id="0545c-131">OUTPUTS</span></span>

### <span data-ttu-id="0545c-132">않아야</span><span class="sxs-lookup"><span data-stu-id="0545c-132">None</span></span>

## <span data-ttu-id="0545c-133">상속자</span><span class="sxs-lookup"><span data-stu-id="0545c-133">NOTES</span></span>

## <span data-ttu-id="0545c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0545c-134">RELATED LINKS</span></span>

[<span data-ttu-id="0545c-135">제거-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="0545c-135">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="0545c-136">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="0545c-136">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


