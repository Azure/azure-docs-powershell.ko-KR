---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: c6d15769891f02a6c1be12a277e17ca2ccba107e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495507"
---
# <span data-ttu-id="f846b-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="f846b-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="f846b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f846b-102">SYNOPSIS</span></span>
<span data-ttu-id="f846b-103">지정된 Data Lake Store 계정의 암호화를 위해 사용자 관리 Key Vault를 사용하도록 설정하려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="f846b-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="f846b-104">구문</span><span class="sxs-lookup"><span data-stu-id="f846b-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f846b-105">설명</span><span class="sxs-lookup"><span data-stu-id="f846b-105">DESCRIPTION</span></span>
<span data-ttu-id="f846b-106">**Enable-AzDataLakeStoreKeyVault** cmdlet은 지정된 Data Lake Store 계정의 암호화를 위해 사용자 관리 Key Vault를 사용하도록 설정하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="f846b-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="f846b-107">예제</span><span class="sxs-lookup"><span data-stu-id="f846b-107">EXAMPLES</span></span>

### <span data-ttu-id="f846b-108">예제 1: ContosoADLS 계정에 Key Vault 사용</span><span class="sxs-lookup"><span data-stu-id="f846b-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="f846b-109">이 명령은 ContosoADLS라는 Data Lake Store 계정에 대해 사용자 관리 Key Vault를 사용하도록 설정하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="f846b-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="f846b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f846b-110">PARAMETERS</span></span>

### <span data-ttu-id="f846b-111">-Account</span><span class="sxs-lookup"><span data-stu-id="f846b-111">-Account</span></span>
<span data-ttu-id="f846b-112">사용자 관리 Key Vault를 사용하도록 설정하기 위한 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="f846b-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="f846b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f846b-113">-DefaultProfile</span></span>
<span data-ttu-id="f846b-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f846b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f846b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f846b-115">-ResourceGroupName</span></span>
<span data-ttu-id="f846b-116">계정과 연결된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f846b-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="f846b-117">지정하지 않으면 검색을 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="f846b-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="f846b-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f846b-118">-Confirm</span></span>
<span data-ttu-id="f846b-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f846b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f846b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f846b-120">-WhatIf</span></span>
<span data-ttu-id="f846b-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f846b-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f846b-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f846b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f846b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f846b-123">CommonParameters</span></span>
<span data-ttu-id="f846b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f846b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f846b-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f846b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f846b-126">입력</span><span class="sxs-lookup"><span data-stu-id="f846b-126">INPUTS</span></span>

### <span data-ttu-id="f846b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f846b-127">System.String</span></span>

## <span data-ttu-id="f846b-128">출력</span><span class="sxs-lookup"><span data-stu-id="f846b-128">OUTPUTS</span></span>

### <span data-ttu-id="f846b-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="f846b-129">System.Void</span></span>

## <span data-ttu-id="f846b-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f846b-130">NOTES</span></span>

## <span data-ttu-id="f846b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f846b-131">RELATED LINKS</span></span>

[<span data-ttu-id="f846b-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f846b-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="f846b-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f846b-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

