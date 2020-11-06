---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 922c7e7055c51990b28b472805a68563c94b3e6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537392"
---
# <span data-ttu-id="2b725-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="2b725-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="2b725-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b725-102">SYNOPSIS</span></span>
<span data-ttu-id="2b725-103">가상 컴퓨터에서 SQL server 키 보관소 자격 증명에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b725-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b725-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b725-104">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b725-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2b725-105">DESCRIPTION</span></span>

## <span data-ttu-id="2b725-106">예제의</span><span class="sxs-lookup"><span data-stu-id="2b725-106">EXAMPLES</span></span>

## <span data-ttu-id="2b725-107">변수</span><span class="sxs-lookup"><span data-stu-id="2b725-107">PARAMETERS</span></span>

### <span data-ttu-id="2b725-108">-사용</span><span class="sxs-lookup"><span data-stu-id="2b725-108">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b725-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="2b725-109">-CredentialName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b725-110">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="2b725-110">-AzureKeyVaultUrl</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b725-111">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2b725-111">-ServicePrincipalName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b725-112">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="2b725-112">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b725-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="2b725-113">-Profile</span></span>
<span data-ttu-id="2b725-114">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="2b725-114">@{Text=}</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b725-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2b725-115">-InformationAction</span></span>
<span data-ttu-id="2b725-116">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="2b725-116">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b725-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2b725-117">-InformationVariable</span></span>
<span data-ttu-id="2b725-118">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="2b725-118">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b725-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b725-119">CommonParameters</span></span>
<span data-ttu-id="2b725-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b725-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b725-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b725-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b725-122">입력</span><span class="sxs-lookup"><span data-stu-id="2b725-122">INPUTS</span></span>

## <span data-ttu-id="2b725-123">출력</span><span class="sxs-lookup"><span data-stu-id="2b725-123">OUTPUTS</span></span>

## <span data-ttu-id="2b725-124">상속자</span><span class="sxs-lookup"><span data-stu-id="2b725-124">NOTES</span></span>

## <span data-ttu-id="2b725-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b725-125">RELATED LINKS</span></span>

