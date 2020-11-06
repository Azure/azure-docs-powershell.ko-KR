---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/enable-azurermdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: 5316a55e29acb8edc5bd102d118eb2bcc53c2c30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532026"
---
# <span data-ttu-id="ef760-101">Enable-AzureRmDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="ef760-101">Enable-AzureRmDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="ef760-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef760-102">SYNOPSIS</span></span>
<span data-ttu-id="ef760-103">지정 된 Data Lake Store 계정 암호화를 위해 사용자가 관리 하는 키 자격 증명 모음을 사용 하도록 설정 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef760-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef760-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef760-104">SYNTAX</span></span>

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef760-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ef760-105">DESCRIPTION</span></span>
<span data-ttu-id="ef760-106">**AzureRmDataLakeStoreKeyVault** cmdlet은 지정 된 Data Lake store 계정 암호화를 위해 사용자 관리 키 자격 증명 모음을 사용 하도록 설정 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef760-106">The **Enable-AzureRmDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="ef760-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ef760-107">EXAMPLES</span></span>

### <span data-ttu-id="ef760-108">예제 1: ContosoADLS 계정에 대해 키 자격 증명 모음 사용</span><span class="sxs-lookup"><span data-stu-id="ef760-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="ef760-109">이 명령은 ContosoADLS 이라는 Data Lake Store 계정에 대해 사용자 관리 키 자격 증명 모음을 사용 하도록 설정 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef760-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="ef760-110">변수</span><span class="sxs-lookup"><span data-stu-id="ef760-110">PARAMETERS</span></span>

### <span data-ttu-id="ef760-111">-계정</span><span class="sxs-lookup"><span data-stu-id="ef760-111">-Account</span></span>
<span data-ttu-id="ef760-112">사용자 관리 키 자격 증명 모음을 사용 하도록 설정 하는 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="ef760-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef760-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef760-113">-DefaultProfile</span></span>
<span data-ttu-id="ef760-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ef760-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef760-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef760-115">-ResourceGroupName</span></span>
<span data-ttu-id="ef760-116">계정과 연결 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef760-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="ef760-117">지정 하지 않을 경우 검색을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef760-117">If not specified will attempt to be discovered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef760-118">-확인</span><span class="sxs-lookup"><span data-stu-id="ef760-118">-Confirm</span></span>
<span data-ttu-id="ef760-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef760-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef760-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef760-120">-WhatIf</span></span>
<span data-ttu-id="ef760-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ef760-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef760-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef760-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef760-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef760-123">CommonParameters</span></span>
<span data-ttu-id="ef760-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef760-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef760-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef760-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef760-126">입력</span><span class="sxs-lookup"><span data-stu-id="ef760-126">INPUTS</span></span>

### <span data-ttu-id="ef760-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ef760-127">System.String</span></span>

## <span data-ttu-id="ef760-128">출력</span><span class="sxs-lookup"><span data-stu-id="ef760-128">OUTPUTS</span></span>

### <span data-ttu-id="ef760-129">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="ef760-129">System.Void</span></span>

## <span data-ttu-id="ef760-130">상속자</span><span class="sxs-lookup"><span data-stu-id="ef760-130">NOTES</span></span>

## <span data-ttu-id="ef760-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef760-131">RELATED LINKS</span></span>

[<span data-ttu-id="ef760-132">새로운 AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ef760-132">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ef760-133">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ef760-133">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

