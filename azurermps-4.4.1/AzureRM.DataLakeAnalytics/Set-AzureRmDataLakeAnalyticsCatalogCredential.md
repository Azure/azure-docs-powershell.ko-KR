---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: e82559ec366809613ba66af4c27a3b944869f074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534143"
---
# <span data-ttu-id="1e800-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="1e800-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="1e800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e800-102">SYNOPSIS</span></span>
<span data-ttu-id="1e800-103">Azure Data Lake Analytics 카탈로그 자격 증명 암호를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e800-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e800-104">SYNTAX</span></span>

### <span data-ttu-id="1e800-105">호스트 이름 및 포트 지정 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1e800-105">Specify host name and port (Default)</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e800-106">전체 URI 지정</span><span class="sxs-lookup"><span data-stu-id="1e800-106">Specify full URI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e800-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1e800-107">DESCRIPTION</span></span>
<span data-ttu-id="1e800-108">Set-AzureRmDataLakeAnalyticsCatalogCredential cmdlet은 Azure Data Lake Analytics 카탈로그와 연결 된 자격 증명 암호를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-108">The Set-AzureRmDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="1e800-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1e800-109">EXAMPLES</span></span>

### <span data-ttu-id="1e800-110">예제 1: 계정에 연결 된 자격 증명 암호 수정</span><span class="sxs-lookup"><span data-stu-id="1e800-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="1e800-111">이 명령은 NewPassword에 지정 된 암호로 자격 증명 암호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="1e800-112">변수</span><span class="sxs-lookup"><span data-stu-id="1e800-112">PARAMETERS</span></span>

### <span data-ttu-id="1e800-113">-계정</span><span class="sxs-lookup"><span data-stu-id="1e800-113">-Account</span></span>
<span data-ttu-id="1e800-114">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="1e800-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="1e800-115">-Credential</span></span>
<span data-ttu-id="1e800-116">수정할 자격 증명의 이름과 현재 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-116">Specifies the name and current password of the credential to modify.</span></span>

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

### <span data-ttu-id="1e800-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="1e800-117">-CredentialName</span></span>
<span data-ttu-id="1e800-118">수정할 자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="1e800-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="1e800-119">-DatabaseHost</span></span>
<span data-ttu-id="1e800-120">자격 증명을 mydatabase.contoso.com 형식으로 연결할 수 있는 외부 데이터 원본의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e800-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1e800-121">-DatabaseName</span></span>
<span data-ttu-id="1e800-122">자격 증명을 보유 하 고 있는 Data Lake Analytics 계정에서 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="1e800-123">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="1e800-123">-NewPassword</span></span>
<span data-ttu-id="1e800-124">자격 증명의 새 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-124">Specifies the new password for the credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e800-125">-포트</span><span class="sxs-lookup"><span data-stu-id="1e800-125">-Port</span></span>
<span data-ttu-id="1e800-126">이 자격 증명을 사용 하 여 지정 된 DatabaseHost에 연결 하는 데 사용 되는 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-126">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e800-127">-Uri</span><span class="sxs-lookup"><span data-stu-id="1e800-127">-Uri</span></span>
<span data-ttu-id="1e800-128">이 자격 증명이 연결할 수 있는 외부 데이터 원본의 전체 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-128">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e800-129">-확인</span><span class="sxs-lookup"><span data-stu-id="1e800-129">-Confirm</span></span>
<span data-ttu-id="1e800-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e800-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e800-131">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e800-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e800-132">-DefaultProfile</span></span>
<span data-ttu-id="1e800-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e800-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e800-134">CommonParameters</span></span>
<span data-ttu-id="1e800-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e800-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e800-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e800-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e800-137">입력</span><span class="sxs-lookup"><span data-stu-id="1e800-137">INPUTS</span></span>

## <span data-ttu-id="1e800-138">출력</span><span class="sxs-lookup"><span data-stu-id="1e800-138">OUTPUTS</span></span>

### <span data-ttu-id="1e800-139">않아야</span><span class="sxs-lookup"><span data-stu-id="1e800-139">None</span></span>

## <span data-ttu-id="1e800-140">상속자</span><span class="sxs-lookup"><span data-stu-id="1e800-140">NOTES</span></span>

## <span data-ttu-id="1e800-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e800-141">RELATED LINKS</span></span>

